# Pages Repo

This is a Jekyll-based GitHub Pages site served from `fweez/pages` (main branch, `/docs` folder). It collects random docs and notes, usually generated from Claude Code sessions.

## Structure

- All Jekyll site files live under `docs/`
- Topic folders inside `docs/` (e.g., `docs/git/`, `docs/aws/`, `docs/python/`)
- Each doc is a `.md` file inside a topic folder
- `docs/index.md` auto-lists all docs grouped by folder using Jekyll Liquid — no manual updates needed

## Adding a doc

1. Pick or create a topic folder under `docs/`
2. Create a `.md` file with Jekyll frontmatter:

```markdown
---
title: Your Doc Title
---

Content here.
```

The `title` field is required — it's what appears in the index listing.

## What not to touch

- `docs/index.md` — auto-generated listing, don't hardcode links into it
- `docs/_config.yml` — no changes needed for normal doc additions
