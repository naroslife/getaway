# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page HTML surprise birthday gift website for Flóra, showcasing a romantic treehouse getaway in Noszvaj, Hungary. The site is entirely self-contained with no build process or dependencies.

## File Structure

- `index.html` - Complete single-page application with embedded CSS and JavaScript
- `images/` - Photo gallery (numbered 1.jpg through 11.jpg)
- `.history/` - Version history snapshots

## Development

**Running locally:**
```bash
# Option 1: Simple HTTP server with Python
python3 -m http.server 8000

# Option 2: Using PHP
php -S localhost:8000

# Option 3: Using Node.js http-server (if installed)
npx http-server -p 8000
```

Then open `http://localhost:8000` in a browser.

**No build step required** - This is a static HTML site. Simply edit `index.html` and refresh the browser.

## Architecture Notes

The page uses a **single-file architecture** with:

- **Embedded CSS** (lines 7-415) - All styles within `<style>` tag
- **Embedded JavaScript** (lines 594-661) - Scroll animations, intersection observers, parallax effects
- **No external dependencies** - Pure HTML/CSS/JS, no frameworks

### Key Sections

1. **Hero** - Full-screen intro with parallax background (`images/1.jpg`)
2. **Reveal** - Location and description
3. **Experience** - 6-card grid of amenities
4. **Gallery** - Responsive image grid with hover captions
5. **Details** - Two-column layout with amenity list
6. **Message** - Personal love letter section
7. **CTA** - Final call-to-action with date reveal

### JavaScript Features

- **Intersection Observer** - Fade-in animations on scroll
- **Parallax scrolling** - Background effects for hero and CTA sections
- **Staggered animations** - Cards and gallery items animate with delays
- **Loading screen** - 1.5s initial loading animation

## Style Guide

**Color Palette:**
- Primary gold: `#d4a574`
- Dark backgrounds: `#0a0a0a`, `#0f0f0f`, `#1a1a1a`
- White text: `#fff`

**Typography:**
- Headings: `'Playfair Display', Georgia, serif`
- Body: `'Georgia', serif`

**Design Philosophy:**
- Luxury aesthetic with dark theme and gold accents
- Responsive design with mobile breakpoint at 768px
- Smooth transitions and animations throughout
- Parallax and scroll-triggered effects for engagement

## Image Requirements

Images should be:
- High-quality JPEGs
- Named numerically (1.jpg, 2.jpg, etc.)
- Optimized for web (current images range 60KB-600KB)
- Aspect ratios suitable for gallery grid (landscape/portrait mixed)
