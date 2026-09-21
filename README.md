# NagaKushal8.github.io

Minimal project wall — education, skills, projects. Single static `index.html`,
no build step, no dependencies (only Google Fonts over CDN).

Used as the GitHub/portfolio link on job applications for AI/ML engineering roles.

## Deploy to GitHub Pages

The repo **must** be named `NagaKushal8.github.io` to be served at the root domain.

```bash
git init
git add .
git commit -m "Minimal project portfolio"
git branch -M main
git remote add origin https://github.com/NagaKushal8/NagaKushal8.github.io.git
git push -u origin main
```

Then: repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
branch `main`, folder `/ (root)`. Live at `https://nagakushal8.github.io` in ~1 minute.

## Editing

Everything is in `index.html`.

- **Colours** — the `:root` CSS variables at the top. A light-mode override sits
  right below in a `prefers-color-scheme` block.
- **Adding a project** — copy any `<article class="card">` block. Two things matter:
  - `data-tags` drives the filter buttons. Space-separated, any of `ai ml swe data`.
    Multiple tags are fine and intentional (a RAG service is both `ai` and `swe`).
  - `<span class="kind" data-k="...">` sets the coloured badge. Use one of
    `ai` (purple) / `ml` (green) / `swe` (blue) / `data` (amber).
- **Ordering** — cards render in DOM order. Strongest project first.
- **Metrics row** — keep it to real, sourced numbers. It is the part a reviewer reads.
