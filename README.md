# Flore Muguet — Personal Website

Static HTML/CSS site for [floremuguet.com](https://www.floremuguet.com/), migrated from WordPress to a fast, dependency-free deployment on Netlify.

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

## Local preview

Serve the project root with any static file server:

```bash
# Python 3
python3 -m http.server 8000

# Node.js (npx)
npx serve .
```

Then open [http://localhost:8000](http://localhost:8000).

## Deploy to Netlify

### Option 1: Git-based deploy (recommended)

1. Push this repository to GitHub/GitLab/Bitbucket.
2. In [Netlify](https://app.netlify.com/), create a new site from the repository.
3. Build settings:
   - **Build command:** *(leave empty)*
   - **Publish directory:** `.` (root)
4. Connect the custom domain `www.floremuguet.com` in Netlify DNS settings.

### Option 2: Manual deploy

Drag and drop the project folder onto the [Netlify Drop](https://app.netlify.com/drop) page.

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

## License

Content © Flore Muguet. All rights reserved.
