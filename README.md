# web-porto-cal — Astro + Tailwind starter

This repository is a minimal starter scaffold for an image-forward portfolio built with Astro and Tailwind CSS. It focuses on shipping a fast static gallery with room to add animations, Lottie, image pipelines, or a headless CMS later.

## Quick start

Install dependencies and run the dev server:

```bash
npm install
npm run dev
```

Open http://localhost:3000

## Project structure

```
.
├─ package.json
├─ astro.config.mjs
├─ tailwind.config.cjs
├─ postcss.config.cjs
├─ README.md
└─ src/
   ├─ pages/
   │  ├─ index.astro       # Landing page (plays looping webm, redirects to /home)
   │  └─ home.astro        # Home / gallery page
   └─ styles/
      └─ global.css        # Tailwind entry
```

Files to edit when building the site:
- `src/pages/index.astro` — main page and layout
- `src/styles/global.css` — add Tailwind utilities and global rules

Notes on the landing page
- Place your background webm at `src/assets/hero.webm` or update the `<source>` `src` in `src/pages/index.astro`.
- The landing `index.astro` uses the Google font "Nova Flat" for the click bar. The click bar navigates to `/home`.

## Recommended workflow & features to add

- Images: Use a CDN / image service (Cloudinary, Imgix, Cloudflare Images) or `sharp` at build-time to generate responsive `srcset` and AVIF/WebP.
- Lazy loading: use `loading="lazy"` and `<picture>` with `srcset` for each image.
- Animations: add `lottie-web` for vector motion or `gsap` for choreography. Use `prefers-reduced-motion` to respect accessibility.
- Optional interactivity: embed `React` or `Solid` components inside Astro where needed (island architecture).
- CMS (future): add Sanity/Contentful/Netlify CMS for editorial workflows; keep data as JSON/MD for now.

## Build & deploy

Build and preview locally:

```bash
npm run build
npm run preview
```

Deploy to Vercel, Netlify, or Cloudflare Pages for fast static hosting and global CDN. Use an image CDN for assets.

## Next steps I can take

- Wire up Tailwind JIT PostCSS step and add a basic `npx tailwindcss init` workflow (I can add config+build scripts).
- Add an image pipeline example using `sharp` + an `astro` integration.
- Add Lottie component and example usage.

Tell me which of the next steps you want me to implement.
