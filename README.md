# Basify

A free, ultra-minimalistic Ghost theme for everyone who appreciates simplicity.

Basify strips away all unnecessary styling to deliver a clean, readable experience that looks like a basic HTML page with monospace fonts. No fancy effects, no distracting colors - just black text on white background.

## Features

- **Ultra-minimal design** - Looks like a basic HTML page with `<pre>` tags
- **Monospace typography** - Courier New and system monospace fonts
- **Black & white only** - No colors, no distractions
- **Fully responsive** - Works on all devices
- **Ghost 5.0+ compatible** - Built for modern Ghost installations
- **Koenig editor support** - All required CSS classes included
- **Lightweight** - Minimal dependencies and small footprint

## Installation

1. Download the latest release from the [releases page](https://github.com/agon-intelligence/basify/releases)
2. Upload the zip file to your Ghost installation via Settings → Design → Upload theme
3. Activate the theme

## Development

### Requirements

- Node.js 18+
- npm or yarn
- Ghost 5.0+

### Setup

```bash
# Clone the repository
git clone https://github.com/agon-intelligence/basify.git
cd basify

# Install dependencies
npm install

# Build the theme
npm run build

# Watch for changes during development
npm run dev

# Create distributable zip
npm run zip
```

### Testing

```bash
# Test theme with gscan
npm test
```

## Customization

Basify follows strict design guidelines to maintain its minimalistic aesthetic:

- **Colors**: Only black (#000) and white (#fff)
- **Fonts**: Monospace only (Courier New, Monaco, Menlo, Consolas)
- **Layout**: 800px centered, single column
- **Styling**: Minimal borders, no shadows, no effects

If you modify the theme, please maintain these principles to preserve the simplistic style.

## Browser Support

Basify works in all modern browsers that support Ghost 5.0+.

## Issues & Support

If you encounter any issues with this theme, please [open an issue](https://github.com/agon-intelligence/basify/issues) in this repository.

## License

This theme is open source and free to use. Please feel free to modify it to your own preferences, but make sure to include the LICENSE file.

Copyright (c) 2024 Hendrik Michaelsen / Agon Intelligence

## Credits

Created and maintained by [Agon Intelligence](https://agon-intelligence.com/)

---

**[Demo](https://agon-intelligence.com/basify)** | **[Issues](https://github.com/agon-intelligence/basify/issues)** | **[License](LICENSE)**