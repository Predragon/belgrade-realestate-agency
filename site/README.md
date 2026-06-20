# Website

A self-contained, responsive multi-page site. No build step or dependencies: open any
`.html` file in a browser, or host the `site/` folder on any static host
(GitHub Pages, Netlify, Vercel).

## Pages
| File | Page |
|---|---|
| `index.html` | Homepage — hero, services, process, stats, gallery, FAQ, contact |
| `guides.html` | Guides index — cards linking to all six articles |
| `buying.html` | How a foreigner buys in Belgrade |
| `reciprocity.html` | The reciprocity rule explained (with SVG diagram) |
| `investing.html` | Investing & the 10-year exemption (with SVG growth chart) |
| `renting.html` | Renting out your apartment from abroad |
| `neighborhoods.html` | Belgrade neighborhood guide (photo grid) |
| `taxes.html` | U.S. vs. Serbia real estate taxes (with SVG comparison) |
| `assets/style.css` | Shared stylesheet for all article pages |

## Features
- Fixed nav (darkens on scroll) + mobile hamburger menu on every page
- Image-led hero on each page, callout boxes, comparison tables, related-articles strips
- Three custom inline **SVG illustrations** (reciprocity diagram, 10-year price-growth chart,
  US-vs-Serbia tax bars) — no external chart library
- Google Fonts (Playfair Display + Inter), gold-on-navy palette
- All images are free-to-use stock from **Pexels**, hot-linked from their CDN (verified to load)

## Before launch — replace placeholders
- Brand name `Belgrade Property Partners` (search/replace across files if you rename)
- `Your name, Founder` in the homepage About section
- Contact details: email `hello@example.com`, phone, office address (CTA + footers)
- Legal registration numbers in every footer (after licensing)
- **Swap Pexels stock for original photography** of your actual listings and Belgrade —
  better trust and SEO, and avoids generic imagery.

## Preview locally
```bash
cd site && python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy to Cloudflare Pages

This is a pure static site — no build step. Two ways to publish:

### Option 1 — Connect the GitHub repo (recommended; auto-deploys on every push)
1. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. Pick `Predragon/belgrade-realestate-agency`
3. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave empty)*
   - **Build output directory:** `site`
   - **Root directory:** *(leave as repo root)*
4. **Save and Deploy.** Every push to `main` then redeploys automatically.

### Option 2 — Direct upload with Wrangler (one-off)
```bash
cd belgrade-realestate-agency
npx wrangler pages deploy site --project-name belgrade-property
```

### After it's live
- Add your custom domain under **Pages → Custom domains** (Cloudflare handles SSL).
- Replace `YOUR-DOMAIN.com` in `robots.txt` and `sitemap.xml` with the real domain.
- `_headers` (security + asset caching) and `404.html` are picked up automatically by Pages.

