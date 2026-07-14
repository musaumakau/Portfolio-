# Copilot Instructions for Portfolio Repository

## Project Overview

This is a personal developer portfolio website built with vanilla HTML5, CSS3, and JavaScript, hosted on GitHub Pages. The portfolio showcases DevOps/cloud engineering expertise, featured projects, writing, and tech stack.

**Repository**: https://github.com/musaumakau/Portfolio-

## Architecture

The project is a static website with a single-page layout:

- **index.html** - Main HTML structure with semantic sections: hero, projects, articles, skills, and footer
- **style.css** - All styling using CSS custom properties and modern layout techniques (CSS Grid, Flexbox)
- **script.js** - Any interactivity logic (currently minimal)
- **assets/** - Directory for images and other static content

### Design System

The site uses a **semantic CSS architecture**:

- **Custom Properties** organize color, typography, spacing, and layout:
  - Colors: background canvas/surface, text foreground, accent (blue)
  - Typography: Inter (sans-serif) and JetBrains Mono (monospace) from Google Fonts
  - Spacing: 8px base unit scale (xs, sm, md, lg, xl, 2xl)
  - Layout: 1200px max-width container with 1.5rem padding
- **Responsive Design**: Mobile-first approach with breakpoints at 480px and 640px
- **Modern Reset**: Minimal reset (not Eric Meyer) targeting practical layout issues, not legacy tags
- **Class Naming**: Semantic, not literal names (e.g., `--color-fg-default` instead of `--color-text-white`)

## Styling Conventions

1. **CSS Organization**: Sections grouped by concern with clear ASCII comment headers
2. **Custom Properties Priority**: Use CSS variables (`var(--*)`) for all design tokens—never hardcode colors, spacing, or sizes
3. **Spacing & Typography Scales**: Always reference `--space-*` and `--font-size-*` variables
4. **Responsive Strategy**: Breakpoints via `@media` blocks at relevant points; mobile defaults, tablet/desktop overrides
5. **Dark Theme**: All colors follow the dark GitHub-inspired palette defined in `:root`

## File Modifications

- **HTML Changes**: Update semantic section structure in index.html; maintain proper heading hierarchy (h1 → h2 → h3)
- **CSS Changes**: Add styles within appropriate section comments; update custom properties in `:root` if adding new tokens
- **Assets**: Place new images in the `assets/` directory; use semantic naming

## Development Notes

- No build tools, bundlers, or package managers—this is vanilla HTML/CSS/JS
- Browser testing: Open `index.html` directly in a browser or use a local HTTP server
- GitHub Pages hosting: The site is deployed from the `main` branch; changes are live immediately upon commit
- No automated testing or linting configured

## Git Conventions

- Commit messages follow semantic prefixes: `style:`, `feat:`, `fix:`, `docs:`, `refactor:`, `perf:`
- Recent commits show a progression of styling work (CSS foundation → layout → spacing → refinements)
- `.gitignore` excludes: macOS artifacts, IDE settings (VS Code, JetBrains), and logs

## Common Tasks

**Update hero content**: Edit the `#hero` section in `index.html` and apply styles in the "Hero" section of `style.css`

**Modify project cards**: Update articles in `#projects` section; grid layout is defined in "Project cards" CSS section

**Change color scheme**: Update custom properties in `:root` (e.g., `--color-accent`, `--color-bg-canvas`)

**Add new sections**: Follow the pattern: semantic HTML structure in `index.html`, container max-width layout in `style.css` under "Section spacing (shared)", and responsive adjustments in `@media` blocks
