# Margarita Aleeva — Landing Page

A modern, responsive one-page portfolio/landing site that presents Margarita Aleeva
as a standout candidate in **communications, marketing & community management**.

Content was sourced from her [Google Sites portfolio](https://sites.google.com/view/margaritaaleeva/)
and restructured into a focused "hire me" landing experience.

## Highlights

- **Editorial design** — Fraunces display type + Inter UI, warm palette, tasteful motion.
- **Self-contained** — plain HTML/CSS/JS, no build step, no dependencies.
- **Sections** — hero, about, expertise, selected work (with live links), references, contact.
- **Accessible & responsive** — skip link, keyboard focus styles, `prefers-reduced-motion`
  support, scroll-spy navigation, and a mobile menu.

## Run it locally

It's a static site — just open `index.html`, or serve it:

```bash
# Python
python3 -m http.server 8000

# or Node
npx serve .
```

Then visit <http://localhost:8000>.

## Add the real photo

Margarita's headshot can't be downloaded automatically (Google Sites blocks direct
image access), so the hero currently shows an elegant **MA** monogram.

To use her real photo:

1. Save the image as `assets/margarita.jpg`.
2. In `index.html`, find the `PHOTO SLOT` comment in the hero and **uncomment** the
   `<img …class="portrait-img" />` line.

The photo will then replace the monogram automatically.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page structure & content |
| `styles.css` | Design system & responsive layout |
| `script.js` | Nav, scroll reveal, scroll-spy, mobile menu |
| `assets/` | Favicon, social cover, (optional) photo |

## Deploy

Drop the folder onto any static host — **Netlify, Vercel, GitHub Pages, Cloudflare Pages** —
no configuration required.
