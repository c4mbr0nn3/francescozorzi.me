# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal portfolio website for Francesco Zorzi built with Astro, featuring a terminal-inspired UI theme using Tailwind CSS v4 and Carbon icons.

## Development Commands

```bash
# Install dependencies
npm install

# Start dev server (runs at localhost:4321)
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview

# Format code with Prettier
npx prettier --write .
```

## Tech Stack

- **Framework**: Astro 5.16.0
- **Styling**: Tailwind CSS v4.1.17 (using `@tailwindcss/vite`)
- **Icons**: astro-icon with @iconify-json/carbon
- **Code Formatting**: Prettier with plugins for Astro and Tailwind

## Architecture

### Styling System

The project uses Tailwind CSS v4's new `@theme` directive in `src/styles/global.css`:

- Custom Tokyo Night inspired color palette defined as CSS variables
- Custom animation keyframes for terminal cursor blink effect
- Colors: `tokyo-bg`, `tokyo-fg`, `tokyo-border`, `tokyo-user`, `tokyo-host`

### Page Structure

Single-page application with all content in `src/pages/index.astro`:

- **personalInfo**: Object containing name, bio, and social links
- **seo**: SEO metadata including Open Graph and Twitter Card tags
- Terminal-style UI with simulated command prompt
- Links styled to resemble Unix file listings (`ls -l`)

### Astro Configuration

Located in `astro.config.mjs`:

- Tailwind CSS integrated via Vite plugin
- astro-icon integration for icon components

### TypeScript

Uses Astro's strict TypeScript configuration (`astro/tsconfigs/strict`)

## Code Formatting

Prettier is configured with:

- `prettier-plugin-astro` for Astro file formatting
- `prettier-plugin-tailwindcss` for class sorting
- Custom parser override for `.astro` files

## Static Assets

Static files go in `public/` directory:

- Currently contains `favicon.svg`
- Add Open Graph image as `og-image.png` (1200x630px) for social media previews

## Content Updates

To update personal information, modify the `personalInfo` and `seo` objects in `src/pages/index.astro`:

- Update `personalInfo.links` to add/remove social links
- Each link requires: `name`, `icon` (Carbon icon name), and `url`
- Update SEO metadata in the `seo` object for proper meta tags
