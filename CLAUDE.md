# gabybudel.github.io

Personal academic/professional homepage for Gabriel Budel (Gaby Budel), hosted on GitHub Pages.

## Project structure

```
index.html     — single-page site (all content and styles inline)
profile.png    — headshot photo
favicon.svg    — GB initials favicon
robots.txt     — allows all crawlers, points to sitemap
sitemap.xml    — single URL entry for the homepage
```

## Goals

- Serve as the canonical web presence for Gabriel Budel / Gaby Budel
- Rank first on Google for searches: "Gabriel Budel", "Gaby Budel"
- Present publications, working papers, thesis, presentations, software, experience, and education

## Design conventions

- Single HTML file — no build step, no frameworks, no external JS
- All CSS is inline in `<style>` inside `<head>`
- Fonts: DM Serif Display (headings) + Outfit (body) via Google Fonts
- Color palette uses CSS variables defined in `:root`
- Warm off-white background (`#f6f4f0`), blue accent (`#2e5d8a`)

## SEO setup

- Google Search Console verified (meta tag in `<head>`)
- JSON-LD `Person` schema with `name: "Gabriel Budel"` and `alternateName: "Gaby Budel"`
- Meta: description, keywords, author, canonical, og:*, twitter:*, profile:*
- sitemap.xml should have `<lastmod>` updated whenever content changes

## Deployment

GitHub Pages — push to `main` branch deploys automatically.
SSH key is not available in the Claude Code terminal; the user must push from their own shell or run `! git push origin main` in the chat.

## Content update checklist

When adding a new publication, presentation, or role:
1. Add the entry in the appropriate `<section>` in `index.html`
2. Update `<lastmod>` in `sitemap.xml` to today's date
3. Commit and push
