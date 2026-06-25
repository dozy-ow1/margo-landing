# Margarita Aleeva — Landing Page

A modern, responsive one-page landing site that presents Margarita Aleeva as a
standout candidate in **communications, marketing & community management**.

Content was sourced from her [Google Sites portfolio](https://sites.google.com/view/margaritaaleeva/)
and restructured into a focused "hire me" experience.

## Highlights

- **Warm editorial design** — Fraunces display + Inter UI, on a brown / butter-yellow
  (`#FFF1B5`) / powder-blue (`#C1DBE8`) / espresso (`#43302E`) palette.
- **Real project previews** — each work card shows a live thumbnail: first slides of the
  Google Slides decks, the JetBrains digest banner, YouTube poster frames (with a play
  badge), and the UNA magazine cover.
- **Recommendations with downloads** — a ready-to-fill section where each reference has a
  quote and a **Download letter (PDF)** button, plus a "Download all references" CTA.
- **Self-contained** — plain HTML/CSS/JS, no build step, no dependencies.
- **Accessible & responsive** — skip link, keyboard focus styles, `prefers-reduced-motion`,
  scroll-spy nav, and a mobile menu.

## Run it locally

Static site — open `index.html`, or serve it:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

> On a remote/Hetzner server, preview via VS Code's **PORTS** panel or an SSH tunnel
> (`ssh -L 8000:localhost:8000 user@host`) — no firewall change needed.

## Deploy to GitHub Pages

A workflow is included at `.github/workflows/pages.yml`. To go live:

1. Push to the `main` branch (the workflow runs on every push).
2. In the repo on GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. The **Actions** tab shows the deploy; the URL will be
   `https://dozy-ow1.github.io/margo-landing/`.

That's it — every later push auto-redeploys. (`.nojekyll` is included so all asset
folders are served as-is.)

## Things to personalise

| What | Where |
| --- | --- |
| **Real photo** (replaces the `MA` monogram) | Save as `assets/margarita.jpg`, then uncomment the `<img>` in the hero `PHOTO SLOT` comment in `index.html`. |
| **Recommendation quotes** | The excerpts in the Recommendations section are placeholders — replace each `<blockquote>` with a real quote. |
| **Reference PDFs** | Replace the placeholder files in `assets/references/` with the signed letters (keep the filenames). See `assets/references/README.md`. |
| **Location line** | "Based in Germany" is inferred from the +49 number — edit in the Contact section if needed. |

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Page structure & content |
| `styles.css` | Design system & responsive layout |
| `script.js` | Nav, scroll reveal, scroll-spy, mobile menu |
| `assets/work/` | Project preview thumbnails |
| `assets/references/` | Downloadable reference letters (PDF) |
| `.github/workflows/pages.yml` | GitHub Pages deploy |
