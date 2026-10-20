# El Bloque

Life-sim freemium prototype set in a Puerto Rico caserío. Related to Mafuteros Supply, but a separate project from the Mafuteros Supply app.

Imported from the Claude Design project (`El Bloque.dc.html`, published as the "El Bloque Mobile Prototype" artifact).

## Files

- `El Bloque.dc.html` — the app (title → caserío pick → create → hub). Full screen on phones, phone-sized column on desktop. Saves your life in the browser (`localStorage`) so "Continuar vida" picks up where you left off.
- `El Bloque Prototype.dc.html` — the original Claude Design prototype with the design notes and phone mockup, kept for reference
- `manifest.webmanifest`, `icon-*.png` — lets people add it to their home screen as an app
- `Avatar.dc.html` — avatar component, pulled in via `<dc-import name="Avatar">`
- `bloque.css` — shared tokens, type, buttons/tags/cards + `@font-face` rules
- `support.js` — Claude Design runtime that renders `.dc.html` files
- `react*.production.min.js` — React 18.3.1, vendored so the page doesn't depend on unpkg
- `fonts/` — Big Shoulders Display, Bricolage Grotesque, Space Mono (woff2)

## Run locally

The runtime fetches `Avatar.dc.html`, so serve the folder over HTTP rather than opening the file directly:

```sh
cd elbloque
python3 -m http.server 8000
# open http://localhost:8000/El%20Bloque.dc.html
```

On Netlify, `netlify.toml` serves the app at `/`.

