# Dr. Chandraman S. Patil — Portfolio

A cinematic, single-page portfolio for a nanophotonics researcher & roboticist. Ultra-black canvas, instrument-emerald accent, oversized editorial typography, and scroll-choreographed motion (Lenis + GSAP ScrollTrigger).

**Built as one self-contained `index.html`** — no build step, no framework, no `npm install`. Open it and it runs.

---

## Quick start

**Option A — the folder (recommended for deploying)**
```
site/
├── index.html
└── assets/        ← portraits + backgrounds
```
Open `site/index.html` in any modern browser, or drop the whole `site/` folder onto Netlify / Vercel / GitHub Pages.

**Option B — the standalone file**
`chandraman-patil-portfolio.html` has every image embedded as base64. It's a single file you can email, open from anywhere, or double-click — nothing external to load except the fonts and motion libraries (from CDN).

> The page needs an internet connection the first time, to pull Google Fonts (Archivo · Instrument Serif · IBM Plex Mono) and GSAP/Lenis from their CDNs. If those are blocked, the page **still works** — it detects the missing libraries and renders a clean, static, fully readable version (no animation) rather than breaking.

---

## What's inside

Eleven sections, in order: **Hero** (name-and-portrait typographic sandwich over a live photonic-interference canvas) → **Identity** → **Journey** (horizontal, pinned timeline) → **Research** (publications as hover-reveal exhibition rows) → **Systems** (four expertise cards with animated SVG diagrams) → **Flagship Work** (four project chapters, ending in a full-bleed HUMRO scene) → **Measures** (animated counters) → **Philosophy** (word-by-word reveal) → **Recognition** → **Trajectory** → **Contact**.

Signature touches: a lab-instrument cursor (dot + trailing ring + soft glow), film grain, a scroll-progress hairline, a right-edge section index, a cinematic preloader, and full `prefers-reduced-motion` support.

All content is **real** — biography, roles, and the publication list (titles, venues, citation counts) are drawn from the Google Scholar profile and portfolio as of **July 2026**: 1,019 citations · h-index 14 · i10-index 23 · 73 works.

---

## Editing the content

Everything is plain HTML — no JSON, no CMS. Search `index.html` for the text you want to change.

| To change… | Find… |
|---|---|
| Name / hero labels | `id="hero"` — the `.name-line` spans and `.hero-meta` blocks |
| Bio paragraphs | `id="identity"` — the `.id-copy` block |
| Timeline entries | `id="journey"` — each `<article class="j-panel">` |
| Publications | `id="research"` — each `<a class="rrow">` (title, `.r-sub` blurb, `.r-badges`, and citation count in `.r-cites`) |
| The five big numbers | `id="numbers"` — the `data-count="…"` attributes |
| Awards | `id="recognition"` — the `<li>` rows |
| Links (email / LinkedIn / Scholar / X) | search for `chandraman.patil@gmail.com` and the social URLs; they appear in the menu, contact section, and footer |

**Swapping a portrait or background:** replace the matching file in `assets/` (keep the filename) — or point the `src`/`url()` at a new path. The three hero angles (`hero-front`, `hero-left`, `hero-right`) are all included; the layout currently uses front (hero) and left (identity). `hero-right.webp` is spare, ready if you want a third plane.

**Retuning the look:** the entire design system lives in the `:root { … }` block at the top of the `<style>`. `--em` is the emerald accent; `--bg` the background; `--gutter` the page margin. Change them once, they cascade everywhere.

---

## A note on the theme

This build is **dark-only by design** — the brief called for an ultra-black cinematic gallery, and the whole palette, the emerald accent, the grain, and the portrait rim-lighting are composed for that. A light "paper" mode is easy to add on top of the existing token system if you'd like both; say the word.

---

## Deploying

- **Netlify / Vercel:** drag the `site/` folder into the dashboard, or connect a repo. No build command; publish directory is the folder itself.
- **GitHub Pages:** commit `index.html` + `assets/` to the repo root (or `/docs`), enable Pages.
- **Any static host / S3:** upload the two items. That's it.

Before going live, set the real domain in the `<link rel="canonical">` and the `og:` / `twitter:` meta tags near the top of `<head>` so link previews render correctly.

---

## Optional: a Next.js / TypeScript port

If you'd rather have this as a component-based, TypeScript + Tailwind project (sectioned components, typed content in a data file, MDX-editable publications, image optimization via `next/image`), I can port it — same visuals and motion, just a maintainable codebase. Ask and I'll scaffold it.
