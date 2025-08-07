# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

### Development
- `pnpm dev` - Start development server at localhost:4321
- `pnpm build` - Build production site to ./dist/
- `pnpm preview` - Preview built site locally
- `pnpm astro` - Access Astro CLI commands

### Package Management
This project uses **pnpm** as the package manager. Always use `pnpm` instead of `npm` or `yarn`.

## Architecture

### Framework
Astro v5.x static site generator with TypeScript support. The project uses file-based routing through the `src/pages/` directory.

### Project Structure
- `/src/pages/` - File-based routing (each .astro file becomes a route)
- `/src/components/` - Reusable Astro components
- `/src/layouts/` - Layout templates that wrap pages
- `/src/assets/` - Build-time optimized assets (images, SVGs)
- `/public/` - Static assets served as-is

### Key Patterns
1. **Component Composition**: Pages import and compose layouts and components
2. **Astro Components**: Use `.astro` files with frontmatter (---) for component logic and HTML-like template syntax
3. **TypeScript**: Strict mode enabled via tsconfig.json extending Astro's strict preset
4. **Styling**: CSS is scoped to components by default using `<style>` tags in .astro files

### Configuration Files
- `astro.config.mjs` - Main Astro configuration (currently minimal)
- `tsconfig.json` - TypeScript configuration extending Astro's strict preset

## Important Notes
- No testing framework currently configured
- No linting or formatting tools set up
- ES modules are used throughout (`"type": "module"` in package.json)
- The project is a clean Astro starter template ready for extension

## Memories
- Lets go