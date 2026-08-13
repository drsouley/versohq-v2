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

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

The `src/content/` directory contains "collections" of related Markdown and MDX documents. Use `getCollection()` to retrieve posts from `src/content/blog/`, and type-check your frontmatter using an optional schema. See [Astro's Content Collections docs](https://docs.astro.build/en/guides/content-collections/) to learn more.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                           | Action                                           |
| :-------------------------------- | :----------------------------------------------- |
| `npm install`                     | Installs dependencies                            |
| `npm run dev`                     | Starts local dev server at `localhost:4321`      |
| `npm run build`                   | Build your production site to `./dist/`          |
| `npm run preview`                 | Preview your build locally, before deploying     |
| `npm run astro ...`               | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help`         | Get help using the Astro CLI                     |
| `npm run build && npm run deploy` | Deploy your production site to Cloudflare        |
| `npm wrangler tail`               | View real-time logs for all Workers              |

## 👀 Want to learn more?

Check out [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## Credit

This theme is based off of the lovely [Bear Blog](https://github.com/HermanMartinus/bearblog/).
