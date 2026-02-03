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

## Adding New Posts

When adding new posts to the feed, always include:

1. **UUID anchor**: Each `<article class="post">` must have a unique UUID-based `id` attribute:
   ```html
   <article class="post" id="post-xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx">
   ```
   Generate a new UUID v4 for each post.

2. **Linkable timestamp**: The time marker in the `post-meta` div must be wrapped in an anchor link pointing to the post's UUID:
   ```html
   <div class="post-meta">
       @username · <a href="#post-UUID-HERE" class="post-time-link">2 hours ago</a>
   </div>
   ```

This allows users (both human and appliance) to share direct links to specific posts.
