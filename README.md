# Old Story – Whiskey Bar (HTML Replica)

Pixel-accurate local mirror of the [Old Story demo site](https://oldstoryhtml.ancorathemes.com/?storefront=envato-elements) by Ancora Themes.

## What's included

- **23 HTML pages** — home, menu, about, news, store, contacts, features, and more
- **CSS & JS** — original theme styles, Revolution Slider, Essential Grid, jQuery plugins
- **120+ images** — sliders, gallery, team photos, backgrounds, logos

## Run locally

```bash
npm start
```

Then open **http://localhost:3000** and navigate to `index.html`.

Or use any static file server:

```bash
npx serve .
python -m http.server 8000
```

## Pages

| Page | File |
|------|------|
| Home 1 | `index.html` |
| Home 2 | `index2.html` |
| Menu | `menu.html` |
| About Us | `about-us-about-us.html` |
| Contacts | `contacts.html` |
| Shop | `store-shop.html` |
| + 17 more feature/news/store pages |

## Notes

- Google Fonts load from the CDN (same as the live demo).
- All 23 pages load with no JavaScript errors and no missing local assets.
- Original theme © Ancora Themes 2015.

## Deviations from the live demo

The original server (Cloudflare) refused to serve a handful of binary assets to
any automated client, so these were reconstructed:

- **Fontello icon font** — rebuilt from the theme's own `fontello.min.css`
  codepoint map so all 247 icon classes resolve. 236 glyphs are exact; 11 use the
  closest visual equivalent (`left-open`/`right-open` arrows, `gpl`,
  `tripadvisor`, and a few form/media icons). See `css/fontello/config.oldstory.json`.
- **Slider Revolution** — the theme ships v5.0 core, but its runtime-loaded
  extension scripts were unavailable; the core and its 9 extensions are a matched
  v5.3.1 set instead.
- **WooCommerce / Essential Grid fonts** — sourced from upstream (GPL) or
  converted from the bundled TTF. `.eot` variants (IE8 only) are absent.

Replacing these with files from an official Envato theme download would make the
copy byte-exact.
