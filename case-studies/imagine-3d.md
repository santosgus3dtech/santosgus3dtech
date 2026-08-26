# Imagine3D Case Study

Private operations monorepo for a 3D-printing workflow.

## Context

Imagine3D needed a more organized local system for product pages, cost calculation, customized 3D files and internal tools. The project grew into a monorepo that connects a public-facing product experience with local production utilities.

The full repository is private because it includes business-specific assets, local deployment details and operational files. This case study summarizes the technical work without exposing sensitive data.

## Main Modules

| Module | Purpose |
| --- | --- |
| `landing-page/` | Brand page and entry point for tools and products. |
| `calculadora-3d/` | Cost calculator, product registration, PDF generation and local admin flows. |
| `gerador-placas-web/` | Web generator for custom 3D products such as QR nameplates and personalized keychains. |
| `produtos/` | Product catalog, cart pages and SEO-friendly product pages. |
| `modelos/` | Static pages for model ideas and searchable product inspiration. |
| `docker-prod/` | Production Docker setup with path-based routing. |

## Technical Highlights

- Node/Express app for calculator, catalog and admin routes.
- Python/FastAPI tool for generating custom 3D output.
- OpenSCAD-based parametric modeling.
- `.3mf` generation for multicolor 3D-printing workflows.
- SEO page generation from product/catalog data.
- Local Windows scripts for starting and stopping multiple services together.
- Docker production setup for Linux deployment.
- Runtime-generated databases, uploads, PDFs and 3D files kept out of Git.

## Architecture

```text
Browser
  |
  |-- /landing/       -> static brand page
  |-- /produtos/      -> catalog and product pages
  |-- /calculadora/   -> calculator/admin app
  |-- /gerador/       -> custom 3D generator proxy
                         |
                         -> FastAPI + OpenSCAD + .3mf builder
```

## What I Learned

- How to turn several local scripts into a more coherent product workflow.
- How to separate source code from generated operational files.
- How to design routes so public pages, admin pages and local tools can live under one domain.
- How to document a private production system in a way that is still reviewable for portfolio purposes.

## Public Demo Plan

The safest public version would be a separate repository with:

- fake catalog data;
- generated sample screenshots;
- a small non-sensitive `.3mf` example;
- no business assets, tokens, customer data, private domains or deployment credentials;
- README sections for architecture, tradeoffs and next improvements.

