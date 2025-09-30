# Assets Directory

This directory contains source assets used during build time by the Astro static site generator.

## Structure

```
assets/
└── brand/
    ├── BRAND_REFERENCE.md  # Brand guidelines and messaging reference
    ├── logo.png            # EventFlux logo
    ├── banner-full.png     # Full banner image
    └── banner-cropped.png  # Cropped banner variant
```

## Usage

- **Import in Astro components**: Assets here are processed by Astro's build pipeline and optimized automatically
- **Brand assets**: All brand-related files (logos, banners, brand guidelines) are in `brand/`
- **Public assets**: For runtime assets that need direct URLs, use `/public/` instead

## Notes

- Brand assets are imported directly in `.astro` files (e.g., `import logo from '../assets/brand/logo.png'`)
- The BRAND_REFERENCE.md file is the single source of truth for all brand messaging and positioning
- For optimized performance, Astro processes these assets during build time