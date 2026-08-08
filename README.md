# Eli Klo Hair Braiding — Website

Live site: **https://eliklo.pages.dev**
Hosting: Cloudflare Pages, auto-deployed from the `main` branch of this repo.

## Structure

```
.
├── index.html          # The entire website — one self-contained file
├── README.md
└── assets/             # Source photos (reference library, not used at runtime)
    ├── logo/
    │   └── logo.jpeg
    ├── gallery/        # gallery-01 … gallery-14  (portfolio photos)
    └── services/       # box-braids, dreadlocks, feed-ins,
                        # knotless-braids, senegalese-twist
```

## How it works

`index.html` is the whole site. All 20 photos are **base64-embedded** inside it, so it
needs no external files, no build step, and no internet connection to render. Open it by
double-clicking and it works.

The `assets/` folder holds the original photos at full quality. Nothing in the site links
to them — they are kept so images can be re-cropped, replaced, or re-embedded later.
Renaming or moving anything in `assets/` will not affect the live site.

## Deploying

Commit to `main` and push. Cloudflare Pages rebuilds automatically within ~30 seconds.
Because `index.html` sits at the repository root, no build command or output directory
needs to be configured.

## Editing

- **Text or layout:** edit `index.html` directly.
- **Adding a photo:** the new image must be base64-encoded and embedded inline — do not
  add an `<img src="assets/...">` reference, as that breaks the standalone-file design.
- **Translations:** the site has a live EN / FR / ES switcher backed by three dictionaries.
  Any text change must be applied to **all three**, or that language will fall out of sync.

## Business details

| | |
|---|---|
| Address | 206A South Main, Quanah, TX 79252 |
| Phone | +1 254 768 8904 |
| Email | Eliklohairbraiding@gmail.com |
| Hours | Mon–Sat 9:00 AM–5:00 PM · Sun 12:00–5:00 PM |
| Social | Instagram & Facebook — "Eli-Klo Hair Braiding" |

## Design system

- **Palette:** porcelain `#F4EEE4` · espresso `#231A16` · gold `#C6A15B` · aubergine `#432338`
- **Typography:** Fraunces (display serif) + Manrope (body / UI)
- **Sections:** Hero → About → Services → Gallery (lightbox) → Contact → Booking → Footer
