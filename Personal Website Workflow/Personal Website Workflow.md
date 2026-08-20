---
title: Personal Website Workflow
tags:
  - project
  - quartz
---

# Personal Website Workflow

My working notes for learning and running my Quartz site (published at `eric-hur-21.github.io/Ericverse`).

---

## What this repo is

Quartz is a static-site generator: it takes Markdown notes in `content/` and builds a website into `public/`. The main folders I care about:

| Folder / file | What it is | When I touch it |
| --- | --- | --- |
| `content/` | My actual notes/pages (the website's text) | Every time I write |
| `quartz.config.yaml` | Site settings: title, theme, plugins, hosting URL | To configure/customize |
| `docs/` | The full official documentation | To learn |
| `quartz/` | Framework source code | Rarely — only for deep customization |
| `public/` | Generated website output | Never by hand (auto-built) |

---

## Reading map (docs, in order)

Read these `docs/` files in this sequence. Each is a Markdown file I can open right here.

**1 — Foundations**
- [ ] `docs/philosophy.md` — why Quartz works the way it does
- [ ] `docs/getting-started/index.md` — the 4-step setup overview
- [ ] `docs/getting-started/installation.md` — install, `npx quartz create`, local preview
- [ ] `docs/getting-started/authoring-content.md` — how to write & organize notes

**2 — Publishing**
- [ ] `docs/hosting.md` — deploy free (GitHub Pages / Cloudflare / Netlify / Vercel)
- [ ] `docs/cli/sync.md` — `npx quartz sync` to push changes
- [ ] `docs/cli/build.md` — building and previewing locally

**3 — Configuration**
- [ ] `docs/configuration.md` — every option in `quartz.config.yaml`
- [ ] `docs/features/index.md` — the menu of features I can turn on
- [ ] Pick features I want: `docs/features/graph view.md`, `full-text search.md`, `backlinks.md`, `darkmode.md`, `callouts.md`, `Latex.md`

**4 — Customization (later)**
- [ ] `docs/layout.md` + `docs/layout-components.md` — page structure
- [ ] `docs/advanced/architecture.md` — how the build pipeline works
- [ ] `docs/advanced/creating components.md` / `making plugins.md` — extend it

---

## My common commands

Run these in a terminal from the repo root (needs Node v22+).

```bash
npx quartz build --serve   # preview locally at http://localhost:8080
npx quartz sync            # commit + push content to GitHub
npx quartz update          # upgrade Quartz to the latest version
```

---

## Workflow: writing a new note

1. Create a `.md` file in `content/` (or a subfolder).
2. Add frontmatter at the top:
   ```
   ---
   title: My Note Title
   tags:
     - topic
   ---
   ```
3. Link to other notes with wikilinks: `[[Other Note]]`.
4. Preview with `npx quartz build --serve`.
5. Publish with `npx quartz sync`.

---

## Running log

_Notes, questions, and decisions as I learn — newest at top._

- **2026-07-12** — Set up this project file. Next: read `docs/philosophy.md` and `docs/getting-started/installation.md`.
