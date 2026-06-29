# Resources Docs

A single-file, zero-dependency documentation app. Everything lives in `index.html` — open it in a browser and you have a self-hosted knowledge base for notes, references, and project docs. Your content is saved in the browser (via `localStorage`) and can be exported to a JSON file for backup or sharing.

No build step, no server, no accounts. Just an HTML file.

## Quick start

Open `index.html` in any modern browser:

```bash
open index.html        # macOS
# or just double-click the file
```

That's it. On first run you'll get a sample space and an example doc to edit or delete.

To restore an existing backup, use the **Import** button in the top bar.

## How it's organized

Content is structured in three levels:

- **Spaces** — top-level groupings shown in the sidebar (e.g. Mobile, Web, Backend, Design). Add one with **+ Add space**.
- **Docs** — pages inside a space. Add one with the **+** next to a space name.
- **Sections** — the building blocks of a doc. Each section is either:
  - **Text** — formatted with a markdown toolbar (bold, italic, headings, lists, links, inline code) and a live preview.
  - **Code block** — with syntax highlighting and a copy button.

## Features

- **Markdown editing** — toolbar, formatting guide, and live preview for text sections.
- **Syntax-highlighted code blocks** with one-click copy.
- **Full-text search** across all docs, with matching snippets in the sidebar.
- **Drag and drop** to reorder spaces, docs, and sections (and move docs between spaces).
- **Dark / light theme** toggle.
- **Archive** — deleted docs go to an archive and are auto-purged after 30 days (restorable until then).
- **Copy page** — copy a whole doc to the clipboard.
- **Rename the site** — click the title in the sidebar.
- **Responsive** — collapsible sidebar on mobile.

## Data & backups

- All content is stored in your browser under the `localStorage` key `wiggl-docs`. It is **local to that browser** — it does not sync and is not stored on a server.
- **Export** writes everything (all spaces, docs, and the archive) to a single JSON file.
- **Import** loads a backup file — note this **replaces** all current content.

> Because data lives in the browser, clearing site data or switching browsers/machines loses your docs. Export regularly to keep a backup.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire application — markup, styles, and logic. |
