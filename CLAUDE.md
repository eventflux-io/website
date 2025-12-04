# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the marketing website repository for **EventFlux** — a pattern-first stream processing engine (CEP) in Rust.

- **Live URL:** https://www.eventflux.io
- **Hosting:** GitHub Pages via GitHub Actions with custom domain
- **Purpose:** Landing pages (Home, About, Contact), light JS interactions, future embeds (video demo), optional blog/changelog

## Technology Stack

- **Framework:** Astro (Static Site Generator)
- **Language:** TypeScript
- **Deployment:** GitHub Actions → GitHub Pages
- **Node Version:** 20.x

## Development Commands

```bash
npm install          # Install dependencies
npm run dev          # Start dev server at localhost:4321
npm run build        # Build production site to ./dist/
npm run preview      # Preview production build locally
```

## Brand Guidelines (Critical)

Always reference `assets/BRAND_REFERENCE.md` for consistent messaging. Key requirements:

### Naming & Positioning
- **Always** pair the brand with category on first mention: **"EventFlux — pattern-first stream processing engine (CEP) in Rust"**
- Use concrete operator nouns: **filters, joins, enrichment, windows, patterns**
- Keep proof-point consistent: **sub-10 ms latency on common workloads**
- Emphasize **engine**, not platform

### Tone
- Concrete over vague
- Builder-friendly, avoid buzzwords
- Confident but not loud
- Let proof points carry the message

### Key Messaging
- Pattern-first by design (CEP is native, not bolted on)
- Rust-fast, predictable latency
- Essential, not excessive (no platform bloat)
- Operates on-prem and Kubernetes
- No broker lock-in

## Content Licensing

This repository uses **dual licensing**:
- **Site code:** MIT License (`LICENSE`)
- **Content (markdown, copy, illustrations, screenshots):** CC BY 4.0 (`CONTENT-LICENSE`)

When creating or modifying content, ensure proper attribution: "EventFlux"

## Deployment

Site deploys via GitHub Actions to GitHub Pages:
- **Settings → Pages:** Source = "GitHub Actions"
- **Custom domain:** `www.eventflux.io`
- **DNS:** CNAME `www` → `eventflux-io.github.io` (at Namecheap)

## Contributing Standards

### Content Changes
- Maintain consistent brand voice from `assets/BRAND_REFERENCE.md`
- Use the five core operators in intros: filters, joins, enrichment, windows, patterns
- Ensure first mention includes full category phrase

### Accessibility Requirements
- Keep headings logical (H1→H2→H3)
- Ensure sufficient color contrast
- Add alt text to every image
- Place images under `/public/images/` with descriptive filenames

### Image Assets
- Brand assets (logo, banner) live in `/assets/` and are imported directly in Astro components
- Public static assets go in `/public/`
- Use descriptive filenames with proper alt text

## Project Structure

```
/
├── .github/
│   └── workflows/
│       └── deploy.yml       # GitHub Actions deployment workflow
├── assets/                  # Brand assets (logo, banner, brand guide)
├── public/                  # Static assets served as-is
├── src/
│   └── pages/
│       └── index.astro      # Landing page
├── astro.config.mjs         # Astro configuration
├── package.json             # Dependencies and scripts
└── tsconfig.json            # TypeScript configuration
```