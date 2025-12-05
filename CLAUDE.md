# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Ghost theme called "basify" - a minimalistic, free theme for the Ghost blogging platform. The theme targets Ghost >= 5.0.0 and follows an extremely simple, clean design philosophy that mimics basic HTML pages with monospace fonts.

## Design Guidelines

**Core Design Philosophy:**
- **Minimalism First**: The theme should look like a basic HTML page using `<pre>` tags
- **Black and White Only**: No colors except black (#000) on white (#fff) background
- **Monospace Typography**: Use 'Courier New', 'Monaco', 'Menlo', or 'Consolas' exclusively
- **No Fancy Styling**: Avoid gradients, shadows, animations, or decorative elements
- **Simple Borders**: Only use basic 1px solid black borders where absolutely necessary
- **Centered Content**: Header logo, navigation, and footer should be centered
- **Image Constraints**: All images must have `max-width: 100%` to stay within page boundaries
- **Single Logo Display**: Logo should appear only once in the header, not duplicated elsewhere

**Visual Style:**
- 800px max-width centered layout
- Underlined links that remove underline on hover
- Gray text (#666) for metadata and secondary information
- Minimal spacing and padding
- No background colors or patterns

**What to Avoid:**
- Neon colors (especially green terminal-style colors)
- ASCII art borders or decorative characters
- Complex layouts or grid systems
- Hover effects beyond text-decoration changes
- Overlapping or overflow issues with images

## Development Commands

**Build and Development:**
- `npm run dev` or `gulp` - Start development mode with file watching (no live reload in MVP)
- `gulp build` - Build CSS and JS assets for production
- `npm run zip` or `gulp zip` - Create a distributable theme zip file in `dist/`

**Testing:**
- `npm test` or `gscan .` - Test theme compatibility with Ghost
- `npm run test:ci` or `gscan --fatal --verbose .` - CI-friendly testing with verbose output

## Architecture

**Template Structure:**
- `default.hbs` - Main layout template with header, navigation, content area, and footer
- `index.hbs` - Homepage template extending default layout (shows site description and cover image)
- `post.hbs` - Individual post template with feature image, title, meta, content, and author
- `page.hbs` - Static page template with conditional title/feature image display
- Templates use Handlebars syntax with Ghost-specific helpers
- `partials/` directory may be created for reusable components

**Asset Pipeline:**
- Source assets in `assets/css/` and `assets/js/`
- Built assets output to `assets/built/`
- CSS processing: PostCSS with autoprefixer and cssnano (no color functions)
- JS processing: Concatenation and uglification via gulp-concat and gulp-uglify
- Sourcemaps generated for both CSS and JS

**Build System:**
- Uses Gulp 5 with CommonJS (not ES modules)
- Watches for changes in `.hbs`, CSS, and JS files
- No live reload in MVP version (removed to minimize dependencies)
- Minimal dependencies: only essential build tools

**Theme Configuration:**
- Supports Ghost's color scheme settings (Light/Dark/Auto) in package.json config.custom
- Logo displayed centered in header
- Cover image support on homepage
- Primary and secondary navigation support
- Compatible with Ghost's pagination system
- Koenig editor CSS classes (.kg-width-wide, .kg-width-full, etc.) included

## Dependencies (MVP)

**Production Dependencies (9 total):**
- `autoprefixer` - CSS browser compatibility
- `cssnano` - CSS minification
- `gulp` - Build system
- `gulp-concat` - JS bundling
- `gulp-postcss` - CSS processing
- `gulp-uglify` - JS minification
- `gulp-zip` - Theme packaging
- `postcss-easy-import` - CSS imports
- `pump` - Stream error handling

## File Structure

**Templates:**
- All templates are in root directory
- `default.hbs` - Base layout
- `index.hbs` - Homepage
- `post.hbs` - Blog posts
- `page.hbs` - Static pages
- `partials/` may contain reusable components (currently may not exist)

**Assets:**
- `assets/css/index.css` - Source CSS
- `assets/js/index.js` - Source JS
- `assets/built/` - Compiled assets (gitignored)

**Build Files:**
- `gulpfile.js` - Build configuration
- `package.json` - Dependencies and scripts
- `dist/` - Theme zip output (gitignored)