# EventFlux Website

Marketing website for **EventFlux** — the pattern-first stream processing engine (CEP) in Rust.

- **Live URL:** https://www.eventflux.io
- **Purpose:** Landing pages (Home, About, Contact), light JS interactions, future embeds (video demo), optional blog/changelog.
- **Hosting:** GitHub Pages (via GitHub Actions) with custom domain `www.eventflux.io`.

---

## Technology Stack

- **Framework:** Astro (Static Site Generator)
- **Language:** TypeScript
- **Deployment:** GitHub Actions → GitHub Pages
- **Node Version:** 20.x

## Development

```bash
# Install dependencies
npm install

# Start dev server at localhost:4321
npm run dev

# Build production site to ./dist/
npm run build

# Preview production build locally
npm run preview
```

---

## What's here

- **Content & pages:** Copy, sections, and simple forms (e.g., contact).
- **Components & layouts:** Header, footer, nav, CTA, hero, feature blocks.
- **Assets:** Favicons, social images (OpenGraph), brand marks.

> For brand language, taglines, and category phrasing, see the internal **Brand & Messaging Reference** (`assets/BRAND_REFERENCE.md`).

---

## Publishing

This site is built and deployed by a GitHub Actions workflow to GitHub Pages.
The repo's **Settings → Pages** is configured to:
- **Build and deployment:** Source = "GitHub Actions"
- **Custom domain:** `www.eventflux.io`
- **Enforce HTTPS:** enabled once DNS is active

DNS (at Namecheap):
- CNAME `www` → `eventflux-io.github.io`
- URL Redirect (301) apex `@` → `https://www.eventflux.io`

---

## Contributing

- **Small copy changes:** open a PR with a clear before/after in the description.
- **New sections/pages:** add a short rationale and proposed placement in the nav.
- **Images:** place under `/public/images/` with descriptive filenames and alt text.
- **Accessibility:** keep headings logical (H1→H2→H3), ensure sufficient color contrast, and add alt text to every image.

### Style & tone

- Always pair the brand with the category on first mention:
  **"EventFlux — pattern-first stream processing engine (CEP) in Rust."**
- Prefer concrete nouns: **filters, joins, enrichment, windows, patterns**.
- Keep the proof concise (e.g., *sub-10 ms latency on common workloads*).

---

## Licensing

This repository uses **dual licensing**:

- **Site code (components, layouts, build config):** MIT — see `LICENSE`
- **Content (markdown, page copy, illustrations, screenshots):** CC BY 4.0 — see `CONTENT-LICENSE`

Please attribute "EventFlux" when reusing content under CC BY 4.0.