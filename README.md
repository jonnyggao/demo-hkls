# HKLS Demo Site

Static HTML/CSS demo for a sales pitch — modern Cantonese language school site targeting expats in Hong Kong.

**Live demo:** [jonnyggao.github.io/demo-hkls](https://jonnyggao.github.io/demo-hkls/) *(after GitHub Pages is enabled)*

## Deploy to GitHub Pages

This repo is set up for [GitHub Pages](https://docs.github.com/en/pages) via GitHub Actions. The workflow in `.github/workflows/pages.yml` publishes only the demo site (`index.html`, `css/`, `assets/`).

### One-time setup

1. Push this repo to GitHub (`jonnyggao/demo-hkls`).
2. In the repo on GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Push to `main` (or run the workflow manually under **Actions → Deploy to GitHub Pages → Run workflow**).

The site will be available at `https://<username>.github.io/demo-hkls/`.

## Open locally

```bash
open index.html
```

Or serve with any static server:

```bash
python3 -m http.server 8080
# Visit http://localhost:8080
```

## Scope (MVP)

- Pure HTML + CSS (no JavaScript)
- English-first, expat-focused Cantonese messaging
- WhatsApp & phone CTAs only (no forms, no login)
- No popups or promotions
- Single-page layout with anchor navigation

## Files

| File | Purpose |
|------|---------|
| `index.html` | Full demo landing page |
| `css/styles.css` | All styles |
| `assets/logo.png` | HKLS logo |
| `assets/favicon.ico` | Site favicon |
| `.github/workflows/pages.yml` | GitHub Pages deploy workflow |
| `.nojekyll` | Disables Jekyll processing on GitHub Pages |
| `HKLS-WEBSITE-AUDIT.md` | Original live-site audit |
