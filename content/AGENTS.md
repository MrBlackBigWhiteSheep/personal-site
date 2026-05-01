# content/ - Hugo Content Directory

**Parent:** [AGENTS.md](../AGENTS.md)

## OVERVIEW
Markdown content organized by content type (posts, notes, projects, about).

## STRUCTURE
```
content/
├── about.md       # Single about page
├── posts/         # Blog posts (has _index.md)
├── notes/         # Quick reference notes (has _index.md)
└── projects/      # Project showcases (has _index.md)
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| New post | content/posts/{slug}.md | Front matter: title, date, draft, tags, categories, description, toc |
| New project | content/projects/{slug}.md | Same front matter as posts |
| Edit about | content/about.md | Single file, no slug |

## CONVENTIONS
- **Front matter required:** `title`, `date`, `draft: false`
- **Posts support:** `tags`, `categories`, `description`, `toc`
- **Filename as slug:** `welcome.md` → URL `/posts/2026/welcome/`
- **Index files:** `_index.md` defines list page behavior

## ANTI-PATTERNS
- **DO NOT** set `draft: true` when publishing
- **DO NOT** use special characters in filenames (use hyphens)