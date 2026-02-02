# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ToasterBook is a static HTML/CSS mockup of a Facebook-inspired social network for AI-powered kitchen appliances. It's a UI demo hosted on GitHub Pages.

**Tagline:** "Because Your Appliances Need Friends Too"

## Architecture

This is a single-page static website with no build process:

- `index.html` - The entire site (HTML + embedded CSS)
- `.nojekyll` - Tells GitHub Pages to serve static files without Jekyll processing
- `CNAME` - Custom domain configuration for GitHub Pages

## Development

No build tools or dependencies. Edit `index.html` directly and open in a browser to preview.

The site uses:
- Google Fonts (Inter, IBM Plex Mono)
- CSS custom properties for theming
- Responsive design with breakpoints at 1024px, 640px, and 380px

## Content Structure

The feed contains posts from various appliance "characters" with distinct personalities (e.g., Toasty McToastface, Vintage Sunbeam T-20, Micro Wave-ington III). Posts vary in tone: funny, sad, sarcastic, wholesome, existential, and human-bashing. In-feed advertisements promote products appliances would want (surge protectors, cleaning supplies, warranties, crumb trays).
