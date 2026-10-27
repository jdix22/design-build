# Fairgrain Design + Build: contractor website template

A one-page website for a design-build general contractor (kitchens, bathrooms, basements, built-ins, decks). It's plain HTML, CSS and JavaScript with no build step, so it runs on GitHub Pages as-is.

## Highlights
- Interactive **before/after slider** with tabs for three projects. You can drag it with a mouse, swipe it on a phone or move it with the arrow keys, and it gives a small nudge the first time it scrolls into view.
- Services, stats, process, about, gallery, reviews, FAQ and a quote form with a thank-you state
- A sticky "Call / Free estimate" bar on phones
- SEO basics: a meta description, Open Graph tags and `GeneralContractor` structured data (JSON-LD)
- Respects reduced-motion settings, and the main controls work from the keyboard

## Publish on GitHub Pages
1. Create a repo and upload `index.html`, `README.md` and the `assets/` folder.
2. Go to **Settings → Pages → Deploy from a branch → main / root**.

## Customizing for a client
- **Business details:** search `index.html` for `Fairgrain`, `Harlow Valley`, `555` and `fairgrainbuild.com`, and update the JSON-LD block in `<head>`.
- **Colours:** change the CSS variables at the top of `<style>` (`--clay` is the accent colour).
- **Before/after photos:** the illustrations are in `assets/before-after/`. To use real photos, add your files and edit the `projects` array near the bottom of `index.html` (the `key` sets the file name, e.g. `kitchen-before.svg`). Before/after pairs taken from the same angle look best.
- **Quote form:** right now it only shows a thank-you message. To have it send email, point it at a service such as Formspree (`<form action="https://formspree.io/f/XXXX" method="POST">`) and remove the `preventDefault` demo handler.

Photos come from [Unsplash](https://unsplash.com) (free to use) and are loaded from their CDN.
