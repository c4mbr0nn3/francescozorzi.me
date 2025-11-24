# francescozorzi.me

A terminal-inspired personal portfolio website built with Astro and styled with Tailwind CSS v4. Features a minimalist design with Tokyo Night color scheme.

## Features

- **Terminal UI Design**: Unix-style command prompt interface
- **Responsive Layout**: Mobile-first design that works on all devices
- **SEO Optimized**: Complete meta tags for search engines and social media
- **Fast Performance**: Built with Astro for optimal loading speeds
- **Type-Safe**: TypeScript support with strict mode
- **Icon System**: Carbon Design System icons via astro-icon
- **Code Formatting**: Prettier configured for consistent code style

## Tech Stack

- [Astro](https://astro.build) 5.16.0 - Static site framework
- [Tailwind CSS](https://tailwindcss.com) 4.1.17 - Utility-first CSS framework
- [astro-icon](https://www.astroicon.dev/) - Icon component system
- [Carbon Icons](https://carbondesignsystem.com/guidelines/icons/library/) - IBM's open-source icon library
- TypeScript - Type safety and better DX

## Quick Start

### Prerequisites

- Node.js 18+
- npm or your preferred package manager

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/francescozorzi.me.git
cd francescozorzi.me

# Install dependencies
npm install

# Start development server
npm run dev
```

Visit `http://localhost:4321` to see your site.

## Development Commands

| Command           | Description                          |
| ----------------- | ------------------------------------ |
| `npm run dev`     | Start dev server at `localhost:4321` |
| `npm run build`   | Build production site to `./dist/`   |
| `npm run preview` | Preview production build locally     |
| `npm run format`  | Format all files with Prettier       |

## Project Structure

```text
/
├── public/
│   └── favicon.svg          # Site favicon
├── src/
│   ├── components/
│   │   └── TerminalPrompt.astro  # Reusable terminal prompt component
│   ├── pages/
│   │   └── index.astro      # Main landing page
│   └── styles/
│       └── global.css       # Global styles and Tailwind theme
├── astro.config.mjs         # Astro configuration
├── tsconfig.json            # TypeScript configuration
├── package.json             # Dependencies and scripts
└── CLAUDE.md               # AI assistant guidance file
```

## Customization

### Update Personal Information

Edit `src/pages/index.astro` and modify the `personalInfo` object:

```javascript
const personalInfo = {
  name: "francesco.zorzi",
  host: "me",
  bio: "your bio here",
  links: [
    { name: "resume.pdf", icon: "carbon:document-pdf", url: "your-url" },
    { name: "linkedin", icon: "carbon:logo-linkedin", url: "your-url" },
    // Add more links...
  ],
};
```

### Update SEO Metadata

Modify the `seo` object in `src/pages/index.astro`:

```javascript
const seo = {
  title: "Your Name | Your Title",
  description: "Your description",
  canonical: "https://yourdomain.com",
  // ... update og and twitter card info
};
```

### Change Color Scheme

Edit the color variables in `src/styles/global.css`:

```css
@theme {
  --color-tokyo-bg: #1a1b26;
  --color-tokyo-fg: #c0caf5;
  --color-tokyo-border: #414559;
  --color-tokyo-user: #7aa2f7;
  --color-tokyo-host: #bb9af7;
}
```

### Add More Icons

Browse the [Carbon Icons library](https://icon-sets.iconify.design/carbon/) and use any icon by its name:

```astro
<Icon name="carbon:icon-name" />
```

## Deployment

The site can be deployed to any static hosting platform:

- [Vercel](https://vercel.com/)
- [Netlify](https://www.netlify.com/)
- [Cloudflare Pages](https://pages.cloudflare.com/)
- [GitHub Pages](https://pages.github.com/)

Build command: `npm run build`
Output directory: `dist`

## License

MIT License - feel free to use this template for your own portfolio!
