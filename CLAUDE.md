# gabybudel.github.io

Personal academic/professional homepage for Gabriel Budel (Gaby Budel), hosted on GitHub Pages.

## Project structure

```
index.html       — single-page site (all content, styles, and JS inline)
v2.2-light.html  — backup design variant (noindex; compact mouse-network style, kept for reference)
profile.png      — headshot photo
favicon.svg      — GB initials favicon
robots.txt       — allows all crawlers, points to sitemap
sitemap.xml      — single URL entry for the homepage
_config.yml      — Jekyll config; excludes CLAUDE.md from the published site
```

## Goals

- Serve as the canonical web presence for Gabriel Budel / Gaby Budel
- Rank first on Google for searches: "Gabriel Budel", "Gaby Budel"
- Present publications, working papers, thesis, presentations, software, experience, and education

## Design conventions

- Single HTML file — no build step, no frameworks, no external JS (small inline scripts only);
  the GoatCounter analytics tag before `</body>` is the one deliberate exception
- All CSS is inline in `<style>` inside `<head>`
- Fonts: Source Serif 4 (name, headings, journal titles) + Hanken Grotesk (body, sidebar) + Spline Sans Mono (year column and link pills only) via Google Fonts
- Headings are upright; italic is reserved for journal and thesis titles
- "Gilded paper" light theme; CSS variables in `:root`: warm off-white background (`#f6f2ea`), ochre gold accent (`#9a7434`), steel blue (`#3f6fa3`)
- Layout: sticky sidebar (name, contact, scrollspy TOC) + ledger-style rows with a year column
- Backdrop: genuine `{6,4}` Poincaré-disk tessellation (hexagons reflected via circle inversion), drawn once by inline JS at load; turns up to 24° over the page via a CSS scroll-driven animation (script fallback with easing for older browsers; none under reduced motion)
- Keep it restrained: no drop caps, progress bars, glows, gradients, or load/scroll animations. Interaction is limited to hover colour changes on rows and links; content is visible without JavaScript
- Publications with companion code get a `code` pill link next to the `doi` pill
- Experience and Education get a timeline (vertical line + dot per entry); other sections don't, since they aren't sequences

## Analytics

- GoatCounter (cookieless, no personal data, so no consent banner) via one async
  `<script>` before `</body>` in `index.html`
- Site code lives in the `data-goatcounter` URL; dashboard at
  `https://gabybudel.goatcounter.com`
- The script skips localhost and `file://`, so local previews are not counted

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
