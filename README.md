# R1V3R5: A River Journal

This repository contains a longform publication platform inspired by Distill with a continuous ASCII river animation on the home page.

## Structure

**`site/`** — The Hugo-based journal and website. This is what gets published. See [design.md](design.md) for the complete design brief and authoring guide.

**`logo-generator/`** — A standalone tool for generating ASCII river logos. It produces both static variants (for branding) and animated sequences (for the site header). See `logo-generator/IMPLEMENTATION-PLAN.md` for technical details. The generated modules are vendored into `site/assets/js/vendor/` and used by the site's header animation.

## Quick Start

From the `site/` directory:

```bash
hugo server -D                           # local development
hugo --minify --cleanDestinationDir      # production build (removes stale fingerprinted assets)
```

Publishing workflow: edit posts under `site/content/posts/`, preview locally, rebuild, and deploy `site/public/`.

## Documentation

- **[design.md](design.md)** — Design brief, site behavior, and complete authoring guide for the journal. Start here.
- **[site/README.md](site/README.md)** — Math and figure authoring reference.
- **[logo-generator/IMPLEMENTATION-PLAN.md](logo-generator/IMPLEMENTATION-PLAN.md)** — Technical details on the ASCII river generator.

## Project Scope

The journal is a static site built with Hugo. Source edits happen in `site/content/`, `site/layouts/`, and `site/assets/`. The animated header logo is loaded via the Hugo asset pipeline and runs browser-side. There's no backend server required—everything deploys as flat HTML.
