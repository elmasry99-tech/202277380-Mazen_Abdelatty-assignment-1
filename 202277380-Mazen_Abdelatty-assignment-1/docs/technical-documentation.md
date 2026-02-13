# Technical Documentation

## Architecture Overview

This portfolio is a single-page application (SPA) built with vanilla HTML5, CSS3, and JavaScript (ES6+). No frameworks or build tools are required — it runs directly in any modern browser.

## File Structure

| File | Purpose |
|------|---------|
| `index.html` | Semantic HTML structure with all portfolio sections |
| `css/styles.css` | Complete styling including responsive design and theming |
| `js/script.js` | All interactive features and DOM manipulation |
| `assets/images/` | Profile photo and project placeholder images |

## Design System

### Color Palette

| Token | Dark Mode | Light Mode |
|-------|-----------|------------|
| `--bg-primary` | `#0a0a0a` | `#fafafa` |
| `--bg-secondary` | `#111111` | `#f0f0f0` |
| `--gold` | `#d4af37` | `#d4af37` |
| `--gold-light` | `#f5c842` | `#f5c842` |
| `--text-primary` | `#f0f0f0` | `#1a1a1a` |
| `--text-secondary` | `#a0a0a0` | `#555555` |

### Typography

- **Headings**: Outfit (Google Fonts) — weights 300–800
- **Body**: Inter (Google Fonts) — weights 300–600

### Layout

- **CSS Grid**: Used for Skills (3-column), Projects (2-column), About (2-column), and Contact (2-column)
- **Flexbox**: Used for Navbar, Hero, Footer, and form layouts
- **Breakpoints**: 1024px (tablet), 768px (mobile), 480px (small mobile)

## JavaScript Features

| Feature | Implementation |
|---------|---------------|
| **Theme Toggle** | `data-theme` attribute on `<html>`, CSS custom properties, `localStorage` persistence |
| **Smooth Scrolling** | `scrollIntoView({ behavior: 'smooth' })` on all `#` anchor links |
| **Time Greeting** | `new Date().getHours()` to determine morning/afternoon/evening/night |
| **Typing Animation** | Recursive `setTimeout` with character-by-character rendering and word cycling |
| **Scroll Animations** | `IntersectionObserver` with 15% threshold, `visible` class toggle |
| **Skill Bars** | Animated width via `data-width` attributes, triggered on intersection |
| **Form Validation** | Regex email validation, length checks, error messages, toast on success |
| **Mobile Menu** | Hamburger toggle with CSS transform animations |
| **Gold Particles** | Dynamically created `div` elements with CSS `@keyframes` float animation |

## Accessibility

- Semantic HTML5 elements (`nav`, `section`, `footer`)
- `aria-label` attributes on icon-only buttons
- `alt` text on all images
- Keyboard-navigable form and links
- Sufficient color contrast in both themes

## Performance

- `loading="lazy"` on images
- CSS `backdrop-filter` with `-webkit-` vendor prefix for Safari
- No external JavaScript libraries — zero dependency overhead
- IntersectionObserver for scroll animations (avoids costly scroll event handlers)
- Google Fonts loaded with `preconnect` for faster rendering
