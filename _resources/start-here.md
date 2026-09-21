---
layout: post
title: How this section works
description: A placeholder entry showing the front matter every resource uses. Delete it once you have real ones.
category: guides
date: 2026-09-21
last_updated: 2026-09-21
tags: [meta]
toc:
  sidebar: left
---

This is a placeholder so the resources page has something to render. Delete this file
once you have real entries.

## Adding a resource

Create a Markdown file in `_resources/`. The filename becomes the URL, so
`applying-to-nsf-grfp.md` is published at `/resources/applying-to-nsf-grfp/`.

The front matter looks like this:

```yaml
---
layout: post
title: Applying to the NSF GRFP
description: One line that appears under the title on the resources index.
category: applications # applications | guides | explainers
date: 2026-09-21 # when you first published it
last_updated: 2026-10-02 # optional; shown instead of date on the index
tags: [fellowships, writing] # optional
toc:
  sidebar: left # optional; a sidebar table of contents, good for long manuals
---
```

Only `title` and `category` really matter. Everything else is optional.

## Categories

The index page groups entries under the categories listed in
`display_categories` in `_pages/resources.md`:

- **applications** — for people applying to things
- **guides** — manuals and how-tos
- **explainers** — explanations of stuff

Rename them, reorder them, or add more by editing that one line. If an entry's
`category` doesn't match anything in that list, it still shows up in an
**other** group at the bottom rather than disappearing.

## Resources vs. blog

Resources are reference material meant to be useful to someone else, and they
get updated over time. The blog stays for personal posts — experiences,
thoughts, whatever you feel like writing.
