# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based personal academic website for Joonhyung Park, deployed on GitHub Pages. It uses the Minimal Mistakes theme (v4.24.0).

## Build Commands

```bash
# Install dependencies
bundle install
npm install

# Development server with auto-reload
rake preview

# Build JavaScript assets
npm run build:js

# Watch JS files for changes
npm run watch:js

# Production build
bundle exec jekyll build
```

## Architecture

- **Jekyll static site** with Kramdown markdown processor
- **Minimal Mistakes theme** configured via `_config.yml`
- **Main content**: `_pages/about.md` serves as the homepage/landing page
- **docs/**: Contains theme documentation and demo content (separate from main site)
- **test/**: Theme preview/test environment

### Key Directories

- `_config.yml`: Main site configuration
- `_pages/`: Custom pages (about.md is primary content)
- `_includes/`: Reusable HTML components (43 files)
- `_layouts/`: Jekyll templates (14 layouts)
- `_sass/`: SCSS stylesheets (Minimal Mistakes theme)
- `_data/`: Navigation and UI text configuration
- `assets/css/main.scss`: Custom font and style overrides

### Services

- **Analytics**: Google Analytics (gtag) - tracking ID in `_config.yml`
- **Search**: Algolia indexing via Travis CI
- **Comments**: Staticman with moderation (configured in `staticman.yml`)

## Content Conventions

- Academic profile page uses extensive YAML front matter
- Publications listed with paper links, venues, and co-authors
- News items formatted as reverse-chronological bullet points
- Custom fonts: Raleway (sans-serif) and Merriweather (serif)
