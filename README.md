# kanishka-portfolio

Source for [kanishka-p.github.io](https://kanishka-p.github.io) — a single-page portfolio site pulling together projects, experience, and skills for Data Analyst / Data Scientist / AI Engineer applications.

Plain HTML/CSS/JS, no build step, no dependencies beyond Google Fonts. `index.html` is the entire site; `assets/` holds the screenshots and résumé it references.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

This repo is meant to be served directly by **GitHub Pages**:

1. Push to `github.com/Kanishka-p/kanishka-p.github.io` (the special user-site repo name — Pages serves it at the bare `kanishka-p.github.io` domain with no extra config)
2. In the repo settings → **Pages**, set source to `Deploy from branch`, branch `main`, folder `/ (root)`
3. Done — no CI needed for a static page like this

## Editing

Update `index.html` directly:
- Project cards live in the `#projects` section — each is a `.proj` article
- Résumé PDF and screenshots live in `assets/`; swap the file and the link/`src` keeps working
- Color/type tokens are CSS custom properties at the top of the `<style>` block (light values on `:root`, dark overrides guarded by `prefers-color-scheme` and `[data-theme]`)
