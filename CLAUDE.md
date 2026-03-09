# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Development
pnpm dev           # Start dev server on localhost:4321
pnpm build         # Type-check, build, generate pagefind index, copy to public/
pnpm preview       # Preview production build
pnpm sync          # Sync Astro content types

# Code quality
pnpm lint          # ESLint
pnpm format:check  # Prettier check
pnpm format        # Prettier write
```

> The build command runs `astro check && astro build && pagefind --site dist && cp -r dist/pagefind public/` — pagefind must run after the build to generate the search index.

## Architecture

This is **AstroPaper**, a static blog built with Astro 5, TailwindCSS 4, and TypeScript.

### Content

Blog posts are Markdown files in `src/data/blog/`. Files prefixed with `_` are excluded by the glob loader. The content collection schema is defined in `src/content.config.ts`. Key frontmatter fields: `title`, `description`, `pubDatetime`, `tags`, `draft`, `featured`.

### Configuration

- **`src/config.ts`** — Central site config (`SITE` object): domain, author, pagination, OG images, timezone, language direction
- **`src/constants.ts`** — Social links and share links

### Routing

- `src/pages/index.astro` — Homepage (featured + recent posts)
- `src/pages/posts/[...slug]/` — Individual post pages (dynamic OG images generated here via `src/utils/generateOgImages.ts`)
- `src/pages/tags/` — Tag index and per-tag listing
- `src/pages/archives/` — Archive pages (can be disabled via `SITE.showArchives`)
- `src/pages/search.astro` — Pagefind-powered search UI
- `src/pages/rss.xml.ts`, `robots.txt.ts` — Generated feeds

### OG Images

Dynamic OG images are generated at build time using Satori + Resvg. Templates are in `src/utils/og-templates/`. Fonts are loaded via `src/utils/loadGoogleFont.ts`. OG generation can be disabled via `SITE.dynamicOgImage`.

### Styling

TailwindCSS 4 is configured via the `@tailwindcss/vite` plugin (no `tailwind.config.ts`). Global styles in `src/styles/global.css`; typography in `src/styles/typography.css`. Light/dark mode uses a CSS class toggle.

### Code Blocks

Custom Shiki transformers in `src/utils/transformers/` provide filename display, diff highlighting, and line highlighting. Configured in `astro.config.ts`.

### Path Alias

`@/*` maps to `src/*` (configured in `tsconfig.json`).
