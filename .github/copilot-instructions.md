# Climate Kitchen Prototype - AI Coding Instructions

## Project Overview
Static educational website for UVM's Climate Kitchen non-credit program. Teaches foundational cooking skills through a planetary health lens using five sustainability tenets (plant forward, integrating tastes & habits, low waste, whole food utilization, local & regional sourcing).

## Architecture & Structure

**Multi-workspace setup**: `Climate-Lab-Prototype/` (HTML content) + `teaching-kitchens-site/assets/` (shared CSS). The `assets/` folder is a separate workspace root.

**Page types**:
- **Index** ([index.html](../index.html)): Landing page with `.hero` section and `.two-col` layout featuring sustainability tenets sidebar
- **Content pages** (empower-enact, mise-en-place, sensory-analysis, sequence-planning, knife-skills, time-temperature): Module-specific lessons using `<article>` containers
- **Utility pages** (about, contact): Site information

## HTML Conventions

**Navigation**: Every page includes identical `<nav class="topnav">` with brand link + 8 navigation items. Copy from [index.html](../index.html#L11-L20) when creating new pages.

**Page titles**: Format is `"[Page Name] • Teaching Kitchens: An Integrated Health Approach"`

**Footer**: Consistent across all pages: `© 2026 Climate Kitchen (UVM) — Non‑credit version prototype. Content adapted from UVM Climate Kitchen resources.`

**HTML entities**: Use `&amp;` for ampersands in visible text (e.g., "Empower &amp; Enact", "Time &amp; Temperature")

**Non-breaking spaces**: Use `‑` (non-breaking hyphen) in compound terms like "research‑informed", "hands‑on", "inquiry‑based" to prevent awkward line breaks

## CSS Architecture

Single stylesheet at [assets/style.css](../../teaching-kitchens-site/assets/style.css) with:
- **CSS variables**: Dark green theme (`--bg:#154734`, `--panel:#00313C`, `--accent:#FFD100`, `--text:#F7F7F7`, `--muted:#aac7c0`)
- **Sticky header**: Uses `position:sticky` with backdrop blur
- **Responsive grid**: `.two-col` uses CSS Grid, collapses to single column at 880px
- **Component classes**: `.hero`, `.sidebar`, `.video.placeholder`, `article` for consistent styling

## Development Workflow

**No build process**: Pure static HTML/CSS. Open any `.html` file directly in browser.

**Asset path**: All pages reference `assets/style.css` via relative link `href="assets/style.css"` from project root.

**Testing**: Check responsive behavior at 880px breakpoint where two-column layouts stack.

## Content Patterns

**Video placeholders**: Use `<div class="video placeholder">Embed video: [Topic] (placeholder)</div>` for future media

**External links**: UVM Climate Kitchen references use `target="_blank" rel="noopener"` for security

**Section structure**:
- `<article>` wraps main content on module pages
- `<section>` for distinct content blocks on index
- `.two-col` + `.sidebar` for main/aside layout patterns

## Key Files
- [index.html](../index.html): Template for navigation, hero, and two-column layouts
- [assets/style.css](../../teaching-kitchens-site/assets/style.css): Complete style system with CSS custom properties
- [about.html](../about.html): Minimal content page example
