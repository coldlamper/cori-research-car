# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static, single-page hybrid/PHEV SUV comparison site deployed via GitHub Pages. No build step, no dependencies, no package manager.

## Development

There is no build, lint, or test process. The entire site is `index.html` with embedded CSS and JS. Vehicle images live in `assets/images/`. To preview, open `index.html` in a browser.

## Deployment

GitHub Pages deploys from the `main` branch root. The `.nojekyll` file disables Jekyll processing. Live at `https://coldlamper.github.io/cori-research-car/`.

## Architecture

- **Single file**: All markup, styles, and scripts are in `index.html`. CSS uses custom properties defined on `:root`. JS handles a lightbox for gallery images and hides broken image links.
- **Responsive breakpoints**: 820px (tablet) and 520px (mobile) via `@media` rules.
- **Images**: Each vehicle has four photos (`{vehicle}-1.jpg` through `{vehicle}-4.jpg`) in `assets/images/`. Gallery links open a `<dialog>` lightbox. Broken images auto-hide via an `error` listener.
- **No external dependencies**: No CDN links, no frameworks, no fonts loaded externally. The site is fully self-contained.
