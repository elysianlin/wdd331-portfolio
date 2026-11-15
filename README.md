# wdd331-portfolio

**Student:** Elysian Lin
**Semester:** Fall 2026
**Live Site:** [Visit my live site](https://elysianlin.github.io/wdd331-portfolio/)

## About

This repository is my portfolio for WDD 331R: Advanced CSS. Each week I add new
pages and styles as I work through the course assignments. The site deploys
automatically to GitHub Pages on every push to `main`.

## Architecture

The homepage (`index.html`) is styled by a layered CSS system in `css/`:

Layer order: `tokens, base, layout, components, utilities`. Later layers win
regardless of selector specificity, which is why utilities always override
components without `!important`.

## Build Tool

This project uses **PostCSS** to bundle and minify the CSS architecture into
`dist/styles.css`.

```bash
npm install
npm run build
```

`dist/styles.css` is committed to the repo as a build receipt. The live site
currently links `css/main.css` directly; `dist/styles.css` is not required for
deployment.

## Pages

- [Home](index.html)
- [Custom Properties and Nesting](unit-1/custom-properties/index.html)
- [Layered Components](unit-2/layered-components/index.html)
- [Visual Effects Showcase](unit-3/visual-effects/index.html)
- [Editorial Layout](unit-4/grid-layouts/editorial.html)
- [Responsive Card Grid](unit-4/grid-layouts/cards.html)
- [Scroll Snap Carousel](unit-4/advanced/snap-carousel.html)
- [Container Query Demo](unit-4/advanced/container-demo.html)
- [Sticky Section Headers](unit-4/advanced/sticky-demo.html)


## Typography

Type tokens live in `css/tokens/variables.css`: a modular scale (minor third at
320px, major third at 1280px) with fluid `clamp()` steps from `lg` up, mapped to
semantic roles (`--font-size-body`, `--font-size-heading-lg`, `--font-size-display`,
etc.). Headings use DM Serif Display (Google Fonts, `font-display: swap`) with a
Georgia fallback; body text uses the system font stack.