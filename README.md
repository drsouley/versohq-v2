# VERSOHQ V2 — Multilingual Technology Advisory Website

Multilingual Astro website for VERSOHQ, independent IT and AI consultants serving small businesses across the UAE. Built with 5 language versions (English, French, Spanish, Dutch, Arabic) and optimized for Cloudflare Workers deployment.

**Live Site:** [versohq.com](https://versohq.com)

## Features

- ✅ **5 Language Versions** — English, French, Spanish, Dutch, and Arabic with RTL support
- ✅ **Dark Theme Design** — Modern, professional UI with brand colors and responsive layout
- ✅ **Component Architecture** — Reusable Astro components (Header, Footer, Layout) for maintainability
- ✅ **SEO Optimized** — Language-specific meta tags, canonical URLs, OpenGraph data, structured schema
- ✅ **Mobile-First Responsive** — Mobile nav toggle, adaptive layouts for all screen sizes
- ✅ **Brand Assets** — Logo, founder photos, consistent styling across all languages
- ✅ **Language Routing** — Clean URL structure: `/` (EN), `/fr/`, `/es/`, `/nl/`, `/ar/`
- ✅ **WhatsApp Integration** — Direct CTA buttons with language-specific links
- ✅ **100/100 Lighthouse Performance** — Static site generation via Astro
- ✅ **Cloudflare Workers Ready** — Deploy as static site to Cloudflare Workers

## Getting Started

### Prerequisites

- Node.js 16.x or higher
- npm or pnpm

### Installation

```bash
# Clone the repository
git clone https://github.com/drsouley/versohq-v2.git
cd versohq-v2

# Install dependencies
npm install

# Start development server
npm run dev
```

The site will be available at `http://localhost:4321` with hot reload enabled.

### Language Versions

Access each language version directly:

- **English** — http://localhost:4321/
- **French** — http://localhost:4321/fr/
- **Spanish** — http://localhost:4321/es/
- **Dutch** — http://localhost:4321/nl/
- **Arabic** — http://localhost:4321/ar/

Language switcher in the header navigation allows quick switching between all 5 versions.

## 🚀 Project Structure

```
versohq-v2/
├── src/
│   ├── pages/
│   │   ├── index.astro              # English homepage (/)
│   │   ├── about.astro              # English about page (/about)
│   │   ├── fr/
│   │   │   └── index.astro          # French homepage (/fr/)
│   │   ├── es/
│   │   │   └── index.astro          # Spanish homepage (/es/)
│   │   ├── nl/
│   │   │   └── index.astro          # Dutch homepage (/nl/)
│   │   ├── ar/
│   │   │   └── index.astro          # Arabic homepage (/ar/)
│   │   ├── blog/
│   │   │   ├── index.astro          # Blog listing
│   │   │   └── [...slug].astro      # Dynamic blog post routes
│   │   └── rss.xml.js               # RSS feed
│   ├── layouts/
│   │   ├── BlogPost.astro           # Blog post layout
│   │   └── TemplateLayout.astro     # Main layout (header, footer, meta)
│   ├── components/
│   │   ├── TemplateHeader.astro     # Reusable header with language selector
│   │   ├── TemplateFooter.astro     # Reusable footer
│   │   ├── Header.astro             # Blog header
│   │   └── ...other components
│   ├── content/
│   │   └── blog/                    # Markdown blog posts (e.g., first-post.md)
│   └── styles/
│       ├── template.css             # Main stylesheet for all 5 languages
│       └── global.css               # Global styles
├── public/
│   ├── fonts/                       # Font files
│   └── *.jpg, *.svg                 # Images (logo, founder photos)
├── astro.config.mjs                 # Astro configuration
├── wrangler.json                    # Cloudflare Workers config
├── tsconfig.json                    # TypeScript config
└── package.json                     # Dependencies and scripts
```

### Key Files

- **TemplateLayout.astro** — Master layout component wrapping all 5 language homepages. Handles meta tags, canonical URLs, OG data, and RTL support for Arabic.
- **TemplateHeader.astro** — Reusable header with logo, navigation menu, language selector (EN/FR/ES/NL/AR), and WhatsApp CTA.
- **TemplateFooter.astro** — Reusable footer with company info, contact details, and language-specific footer links.
- **template.css** — 700+ line stylesheet with dark theme, responsive breakpoints, component classes, and CSS custom properties for theming.
- **Language Pages** — Each language version (index.astro, fr/index.astro, etc.) contains full VERSOHQ homepage content translated into that language.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                           | Action                                           |
| :-------------------------------- | :----------------------------------------------- |
| `npm install`                     | Installs dependencies                            |
| `npm run dev`                     | Starts local dev server at `http://localhost:4321` |
| `npm run build`                   | Build production site to `./dist/` (all 5 languages) |
| `npm run preview`                 | Preview production build locally before deploying |
| `npm run astro ...`               | Run Astro CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help`         | Get help using the Astro CLI                     |
| `npm run build && npm run deploy` | Build and deploy to Cloudflare Workers           |
| `npm run wrangler tail`           | View real-time logs from Cloudflare Workers      |

### Development Workflow

```bash
# Start dev server with hot reload
npm run dev

# In another terminal, check for TypeScript errors
npm run astro check

# When ready to deploy
npm run build
npm run preview    # Test the build locally
npm run deploy     # Deploy to Cloudflare Workers
```

## 🌍 Localization & Language Support

All 5 language versions share the same component architecture and styling:

- **English** — Default language at root (`/`)
- **French** — `/fr/` with French translations and menus
- **Spanish** — `/es/` with Spanish translations and menus
- **Dutch** — `/nl/` with Dutch translations and menus
- **Arabic** — `/ar/` with Arabic translations, RTL layout, and Arabic menus

### Adding a New Language

To add a new language (e.g., German):

1. Create `src/pages/de/index.astro`
2. Copy the structure from an existing language page (e.g., `fr/index.astro`)
3. Translate all content sections
4. Update the language code in frontmatter to `lang="de"`
5. Add language option to TemplateHeader.astro language selector
6. Add German locale to TemplateLayout.astro's `langMap` object

### SEO & Multi-language Setup

- **Canonical URLs** — Each language version has proper canonical tags pointing to itself
- **OpenGraph Locales** — Configured per language (en_US, fr_FR, es_ES, nl_NL, ar_AE)
- **Language Attribute** — Each page has correct `<html lang="xx">` and `dir="rtl"` for Arabic
- **Structured Data** — Schema.org FAQ and Organization data included on all pages
- **Sitemap** — Generated via `@astrojs/sitemap` with all language variants

## � Styling & Design

The website uses a dark theme with:

- **Color Tokens** — CSS custom properties defined in `:root` for easy theming
  - Primary background: `#000000`
  - Surface colors: `#0D0D0F`, `#17181B`
  - Accent colors: `#E5DBF6` (purple), `#4E9AF1` (blue)
  - Card gradients: `#8AB4F8` (p1), `#F6C177` (p2), `#7FE0C0` (p3)
- **Typography** — Plus Jakarta Sans (body) + JetBrains Mono (code)
- **Responsive Breakpoints** — Max-width 1024px (tablet/mobile nav) and 640px (mobile stack)
- **Components** — Buttons, cards (3 variants), hero section, footer, FAQ accordion

All styling is in `src/styles/template.css` and imported by TemplateLayout.astro.

## 🚀 Deployment

This site is built for deployment on **Cloudflare Workers** as a static website:

```bash
# Build static site
npm run build

# Deploy to Cloudflare
npm run deploy
```

Alternatively, deploy the `./dist/` folder to any static hosting provider (Netlify, Vercel, AWS S3, etc.).

### Environment Variables

No environment variables required for the basic site. If adding backend features, configure in:
- `wrangler.json` — Cloudflare Workers configuration
- `.env.local` — Local development variables (not committed)

## 👥 About VERSOHQ

VERSOHQ provides independent IT and AI consulting for small businesses across the UAE. Founded by Suleiman and Vera, the company specializes in:

- **AI Tool Adoption** — Right AI tools for your team, set up and verified
- **Equipment & SaaS** — Best hardware and software for your actual work
- **Digital Presence** — Reliable hosting, business email, and professional web presence

**No vendor commissions** — Advice is driven solely by what works best for your business.

**Contact**
- WhatsApp: +971 56519 5654
- Email: hello@versohq.com
- Website: https://versohq.com

## 🧪 Testing

```bash
# Run Astro type checking
npm run astro check

# Build and preview
npm run build
npm run preview

# Visit each language version
# http://localhost:3000/        (EN)
# http://localhost:3000/fr/     (FR)
# http://localhost:3000/es/     (ES)
# http://localhost:3000/nl/     (NL)
# http://localhost:3000/ar/     (AR)
```

## 📚 Resources & Documentation

- [Astro Documentation](https://docs.astro.build) — Learn Astro framework
- [Astro Discord](https://astro.build/chat) — Community support
- [Cloudflare Workers Docs](https://developers.cloudflare.com/workers/) — Deployment docs
- [MDN Web Docs](https://developer.mozilla.org/) — Web standards reference

## 📝 License

This project is proprietary to VERSOHQ. All rights reserved.
