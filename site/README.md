# Website

`index.html` — a self-contained, responsive homepage. No build step or dependencies:
just open the file in a browser, or host it anywhere static (GitHub Pages, Netlify, Vercel).

## Features
- Fixed nav that darkens on scroll + mobile hamburger menu
- Full-screen hero with Belgrade cityscape, trust bar, about split, 6 service cards
  (one per buyer guide), 4-step process, market stats, photo gallery, FAQ accordion, CTA, footer
- Google Fonts (Playfair Display + Inter), gold-on-navy palette
- All images are free-to-use stock from **Pexels**, hot-linked from their CDN

## Before launch — replace placeholders
- Brand name `Belgrade Property Partners` (search/replace if you choose a different name)
- `Your name, Founder` in the About section
- Contact details: email `hello@example.com`, phone, office address (in the CTA + footer)
- Legal registration numbers in the footer (after licensing)
- Service-card links currently point to `#contact` — repoint to the published guide pages
- **Swap Pexels stock for original photography** of your actual listings and Belgrade —
  better trust and SEO, and avoids generic imagery.

## Preview locally
```bash
cd site && python3 -m http.server 8000   # then open http://localhost:8000
```
