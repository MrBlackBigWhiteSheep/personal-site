# PROJECT KNOWLEDGE BASE

**Generated:** 2026-04-30
**Type:** Hugo Static Site (hugo-PaperMod theme)

## OVERVIEW
Personal website for PhD learning notes, projects, and knowledge management. Built with Hugo, deployed to GitHub Pages via GitHub Actions.

## STRUCTURE
```
./
├── archetypes/           # Content templates
├── assets/css/extended/  # Custom CSS overrides (custom.css)
├── content/              # Markdown content
│   ├── about.md          # About page
│   ├── posts/            # Blog posts
│   ├── notes/            # Quick reference
│   └── projects/         # Project showcases
├── layouts/              # Hugo template overrides
├── static/               # Static files
├── themes/               # Hugo themes (hugo-PaperMod submodule)
├── .github/workflows/    # CI/CD (deploy.yml)
├── hugo.toml             # Main config
└── deploy.yml            # GitHub Actions workflow
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| Edit site config | hugo.toml | baseURL, theme, params, menu |
| Add custom CSS | assets/css/extended/custom.css | Auto-merged by PaperMod |
| Add post | content/posts/{slug}.md | Front matter required |
| Add project | content/projects/{slug}.md | Same as posts |
| Edit about | content/about.md | Single page |
| Deploy workflow | .github/workflows/deploy.yml | Hugo build + Pages deploy |
| Override templates | layouts/ | Mirror theme structure |

## CONVENTIONS
- **Content:** Markdown with YAML front matter (`title`, `date`, `draft: false`)
- **Theme:** hugo-PaperMod via git submodule
- **CSS overrides:** Place in `assets/css/extended/` (auto-merged)
- **Locale:** zh-CN
- **Permalinks:** posts → `/posts/:year/:slug/`, notes → `/notes/:slug/`

## ANTI-PATTERNS
- **DO NOT** edit files in `themes/hugo-PaperMod/` directly
- **DO NOT** commit `public/` (gitignored build output)
- **DO NOT** use `static.yml` for deployment (use `deploy.yml`)

## COMMANDS
```bash
hugo server          # Local dev server
hugo --minify        # Build production
git submodule update --remote themes/hugo-PaperMod  # Update theme
```

## NOTES
- GitHub Pages must be enabled in repo Settings → Pages → Source: GitHub Actions
- Custom theme uses Source Serif 4 (headings) + IBM Plex Sans (body) fonts
- HomeInfoMode enabled for homepage profile display