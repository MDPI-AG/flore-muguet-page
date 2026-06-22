[![Netlify Status](https://api.netlify.com/api/v1/badges/8f5f2ad6-52c3-4376-937f-84e36d69bedc/deploy-status)](https://app.netlify.com/projects/floremuguet/deploys)

# Flore Muguet — Personal Website

Static HTML/CSS site for [floremuguet.com](https://www.floremuguet.com/), deployed on [Netlify](https://floremuguet.netlify.app) and migrated from WordPress.

## Overview

A single-page biography site for Flore Muguet, doctor in social anthropology affiliated with the GSRL laboratory in Paris. The site presents academic profile links, a portrait, biography text, and a downloadable French CV.

## Project structure

```
.
├── index.html              # Main page
├── css/
│   └── styles.css          # Site styles
├── assets/
│   ├── portrait.jpg        # Optimized portrait (600×900)
│   ├── portrait.webp       # WebP variant for modern browsers
│   ├── favicon.svg         # Site favicon
│   └── cv-flore-muguet-2026.pdf
├── robots.txt              # Search engine directives
├── sitemap.xml             # XML sitemap
├── netlify.toml            # Netlify deployment config
└── README.md
```

## Deployment

This site is deployed on Netlify at [https://floremuguet.netlify.app](https://floremuguet.netlify.app).

The production domain [https://www.floremuguet.com](https://www.floremuguet.com) is configured as a custom domain (CNAME) pointing to the Netlify site. Netlify handles HTTPS for both the `*.netlify.app` subdomain and the custom domain.

⚠️ Changes to this GitHub repository are automatically deployed to Netlify (typically within 2-3 minutes).

## SEO

- Semantic HTML5 with proper heading hierarchy
- Meta description, canonical URL, Open Graph, and Twitter Card tags
- JSON-LD structured data (`Person` + `WebPage` schema)
- `robots.txt` and `sitemap.xml`
- Optimized images with WebP via `<picture>` element

## What was removed from WordPress

- Search functionality
- Comments section
- WordPress theme/plugin dependencies
- Analytics scripts (Matomo was on the old site — re-add separately if needed)

## Updating content

Edit `index.html` directly for text changes. Replace files in `assets/` for new portrait or CV versions, then update the `lastmod` date in `sitemap.xml` if needed.

## Local preview

Serve the project root with any static file server:

```bash
# Python 3
python3 -m http.server 8000

# Node.js (npx)
npx serve .
```

Then open [http://localhost:8000](http://localhost:8000).

## License

Content © Flore Muguet. All rights reserved.
