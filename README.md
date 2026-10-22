# Yolo — static UI

A fully self-contained, script-free landing page (branded **YOLO**).
Every resource (images, fonts, CSS, favicon, team logos) is served locally
from `assets/`.

- **No JavaScript** — nothing can crash on click/tap/scroll.
- **Every click redirects to https://yolo365s.co/** — nav, cards, buttons,
  icons: all interactive elements funnel to the brand site.
- **Responsive** — mobile-first app shell (max-width 440px) that centers
  itself on desktop, exactly like the original.

## Structure

```
site/
  index.html            the whole page (view-only UI)
  assets/
    index-CGk9AQ9Q.css  all styles
    logo.png, *.jpg     banners, hero image, icons
    favicon.ico
    teams/              team logos
    fonts/              50 Manrope webfonts
    rewards/            reward image used by CSS
```

## Deploy on Vercel (recommended)

### Option A — drag & drop (no CLI)
1. Go to https://vercel.com/new
2. Drag this `site/` folder onto the page (or "Browse" and pick it)
3. Click **Deploy** — done. No build settings needed.

### Option B — Vercel CLI
```
npm i -g vercel
cd site
vercel --prod
```
When prompted, accept defaults (Framework: **Other**, no build command,
output dir = `./`).

## Other static hosts
Upload this folder as-is to Netlify Drop, Cloudflare Pages, GitHub Pages,
S3/CloudFront, Firebase Hosting, or any web root. Only `index.html` and
`assets/` are required.

## Local preview
```
npx serve .            # or: python -m http.server 8080
```
