# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a GitHub Pages personal portfolio site (`Guille87.github.io`) for Guillermo Amado Díaz, a game/mobile developer. It is a static site with no build system, no package manager, and no dependencies.

## Structure

- `index.html` — the entire site: markup, CSS (in a single `<style>` block), and JS (in a single `<script>` block) all live in this one file.
- `favicon.png` — favicon and social preview image (referenced by `og:image`).

There is no CSS/JS bundler, no framework, and no test suite. Google Fonts (Cinzel, Work Sans, JetBrains Mono) are loaded via `<link>` from `fonts.googleapis.com`.

## Development

Since this is a single static HTML file, there is no build/lint/test step — just edit `index.html` directly and open it in a browser (or serve the directory, e.g. `python3 -m http.server`) to preview.

Changes pushed to the default branch deploy automatically via GitHub Pages.

## Content notes

- The page content (copy, project descriptions, timeline entries in `#cronica`, skill bars in `#habilidades`) is in Spanish (`lang="es"`).
- Skill proficiency bars use inline `width:` percentages on `.bar-fill` elements paired with a `.stat-tag` label (`AVANZADO` / `SÓLIDO`) — keep the label and bar width in sync when editing.
- Project cards (`#proyectos`) use `.project-status` with modifier class `.paused` for inactive projects — status text, badge color, and dot color are tied to that class.
- The `.reveal` class + `IntersectionObserver` in the inline script drives scroll-in fade animations for each section; `prefers-reduced-motion` disables both this and the ember particle animation.
