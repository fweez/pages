# Pages Repo

This is a Jekyll-based GitHub Pages site served from `fweez/pages` (main branch, root). It collects random docs and notes, usually generated from Claude Code sessions.

## Structure

- Topic folders at repo root (e.g., `git/`, `aws/`, `python/`)
- Each doc is a `.md` file inside a topic folder
- `index.md` auto-lists all docs grouped by folder using Jekyll Liquid — no manual updates needed

## Adding a doc

1. Pick or create a topic folder
2. Create a `.md` file with Jekyll frontmatter:

```markdown
---
title: Your Doc Title
---

Content here.
```

The `title` field is required — it's what appears in the index listing.

## What not to touch

- `index.md` — auto-generated listing, don't hardcode links into it
- `_config.yml` — no changes needed for normal doc additions
