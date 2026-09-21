---
layout: page
title: resources
permalink: /resources/
description: Manuals, guides, and explainers—the things I wish someone had written down for me.
nav: true
nav_order: 3
display_categories: [applications, guides, explainers]
---

<!-- pages/resources.md -->
<div class="resources">

{% assign sorted_resources = site.resources | sort: "title" %}

{% if sorted_resources.size == 0 %}

  <p>Nothing here yet. Add a Markdown file to <code>_resources/</code> to get started.</p>

{% else %}

{% for category in page.display_categories %}
{% assign categorized = sorted_resources | where: "category", category %}
{% if categorized.size > 0 %}
<a id="{{ category }}" href=".#{{ category }}">

<h2 class="category">{{ category }}</h2>
</a>
<ul class="post-list">
{% for resource in categorized %}
{% include resource.liquid %}
{% endfor %}
</ul>
{% endif %}
{% endfor %}

  <!-- Anything whose category isn't in display_categories still shows up here,
       so an entry can never silently vanish from the page. -->

{% assign uncategorized = sorted_resources %}
{% for category in page.display_categories %}
{% assign uncategorized = uncategorized | where_exp: "item", "item.category != category" %}
{% endfor %}
{% if uncategorized.size > 0 %}
<a id="other" href=".#other">

<h2 class="category">other</h2>
</a>
<ul class="post-list">
{% for resource in uncategorized %}
{% include resource.liquid %}
{% endfor %}
</ul>
{% endif %}

{% endif %}

</div>
