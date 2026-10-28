# Instructions for Organizing and Updating Clippings

## Overview

A personal notes organizer maintained by opencode. This folder *is* the Obsidian vault for clipped notes — open it in Obsidian directly, and it also builds and publishes as a Zensical site on GitHub Pages.

The Obsidian Web Clipper drops new `.md` files directly into this folder (the repo root). Each file has YAML frontmatter, including a `tags` field. The `tags` field drives the organization: each tag maps to a topic page in `notes/`. `notes/` is the site's `docs_dir`.

Prioritize the ability to search and recall specific items.

## Folder structure

```
- (repo root)        -- Obsidian vault + clippings inbox; new clipped .md files land here
- processed/         -- ingested clippings moved here after processing (gitignored, stays local, never pushed)
- notes/             -- markdown pages for the organized topic notes; also the site docs_dir
- notes/index.md     -- table of contents of all the notes pages + "Latest Finds"
- notes/log.md       -- append-only record of all operations
- notes/Catalog.md   -- auto-generated inventory of all topic pages (do not edit by hand)
```

## Workflow

Always `git pull` to fetch the latest changes from GitHub first.

- Look at all `.md` files in the repo root (new clippings).
- Process each file and all notes inside using the processing instructions below.
  Read each one whole; if you only need part of a file, use the read tool's own
  line limit (or a shell command) — never pass a pipe such as `| head -30` as part
  of a file path, because it is treated as a filename and fails.
- Once processed, move the original file to the `processed/` folder (gitignored). Note: the clipping is ingested into `notes/` as brief, searchable topic entries; the full source clipping stays in `processed/` for reference.
- **Site constraint**: `notes/` is the site's `docs_dir`. Any `.md` file linked from a topic page (e.g. a long bibliography or source document) must also live inside `notes/` for the link to resolve on the published site. If a clipping's content is linked rather than summarized inline, copy the file into `notes/` before moving the original to `processed/`.

## Processing Instructions

When the user adds a new clipped `.md` file to the repo root and asks you to ingest it:

* Read the new file's YAML frontmatter, especially the `tags` field.
* Write an accurate 1-2 line description. If the clipping already contains an
  abstract or summary, use it; only visit the `source` URL when the clipping
  lacks enough detail.
* Identify the main topic from the frontmatter tags.
* Read `notes/index.md` first to find relevant topic pages.
* Map each frontmatter tag to a topic page:
  - `fire`, `wildfire` → `Fire`
  - `software`, `knowledge-base` → `Software`
  - `geospatial`, `spatial` → `Geospatial`
  - `remote`, `remote sensing` → `Geospatial`
  - `insurance` → `Insurance`
  - *any other tag* → create a new topic page named Title_Case from the tag
  - *untagged/empty tag* → `Misc`
* Add a new item to the main topic page, keeping newer notes at the top.
* Add back-links ([[page-name]]) to connect related topics. If a related topic page does not exist, create it.
* Update `notes/index.md` with new pages and one-line descriptions (grid cards).
* Record the change in `notes/log.md`. The file is **newest-first**: insert the new
  entry at the top, immediately below the `---` rule — do not append at the bottom.
  Also update the `**Last updated**` date at the top of the file.

## Update the Website

This folder is published as a Zensical site on GitHub Pages via GitHub Actions (`.github/workflows/deploy.yml`, which runs `python build.py`). After ingesting new notes:

- Update the "Latest Finds" section in `notes/index.md` with the 3 most recently added notes, each from a different topic page. Don't pick these from Misc.
- Commit and push to GitHub (`git add`, `git commit`, `git push`) so the site rebuilds and redeploys automatically. `processed/` stays gitignored and is never pushed.

## Topic Page Format

Every note topic page should follow this structure:

```markdown
# Page Title

**Summary**: One to two sentences describing this page.
**Last updated**: Date of most recent update.

---

- [title](url): description. Related: [[Other_Topic]]. Keywords: keyword one, keyword two
```

## Note Formatting Instructions

- Use Markdown format for each note.
- Use a bullet point for each note.
- For notes with URLs:
  - Format: `[title](url): <description> <keywords>`
  - Add a 1-2 line description from the URL.
- For notes with just text:
  - Format: `*Title*: <description> <keywords>`
  - For notes up to 100 characters, add verbatim. For longer notes, summarize to 100 characters.
- Add 3-6 keywords that best describe the note and aid recall.
- Link related topics using [[wiki-links]] throughout the text.

## Rules

- Keep page filenames Title Case with underscores (e.g. `Confinance.md`), matching the `[[Page_Name]]` used in Related links.
- Write in clear, plain language.
- Always update `notes/log.md` after changes.
