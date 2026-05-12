# cttech-website

Static landing page for [cttech.au](https://cttech.au) — deployed as a Cloudflare Pages site.

## What it is

A single-page marketing site for ctTech, an Australian technology services business. The page cycles through the services on offer using an animated typewriter effect against a cyberpunk matrix-rain background.

Services listed:

- Modern technology solutions
- Digital services
- Website design
- Professional email for business
- General IT support
- Photo digitization

## Tech

| Thing | Detail |
|---|---|
| Markup | HTML5 |
| Styles | CSS3 (single file, no preprocessor) |
| Scripts | Vanilla JS — matrix canvas animation inline in `index.html` |
| Fonts | [Orbitron](https://fonts.google.com/specimen/Orbitron) (logo) + [Inter](https://fonts.google.com/specimen/Inter) (body), loaded from Google Fonts |
| Typing effect | [typed.js 2.0.12](https://cdn.jsdelivr.net/npm/typed.js@2.0.12) via jsDelivr CDN |
| Hosting | Cloudflare Pages |

No build step. No npm. No framework. Edit a file, push, done.

## Structure

```
cttech-website/
├── index.html        Single-page site (HTML + inline JS)
├── css/
│   └── style.css     All styles
└── img/
    └── favicon.png   Browser tab icon
```

## Local development

Open `index.html` directly in a browser — everything loads from CDN or relative paths so a local server is not required. If you want live-reload:

```bash
npx serve .
# or
python3 -m http.server
```

## Deployment

The site deploys automatically via Cloudflare Pages on every push to `main`. Cloudflare serves the static files directly from the repo — no build command is configured.

To connect a fresh Cloudflare Pages project:

1. Link the GitHub repo in the Cloudflare Pages dashboard.
2. Leave the build command and output directory blank (no build step).
3. Cloudflare will serve `index.html` at the root.
