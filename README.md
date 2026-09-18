# Posters

[![Deploy GitHub Pages](https://github.com/RKeelan/Posters/actions/workflows/deploy-pages.yml/badge.svg)](https://github.com/RKeelan/Posters/actions/workflows/deploy-pages.yml)

One-page HTML reference posters, each dense enough to answer most questions about its subject without scrolling and laid out to print on a single sheet. Read them at <https://rkeelan.github.io/Posters/>.

Every poster is a self-contained HTML file: no build step, no framework, no external resources.

## Adding a poster

- Drop the HTML file at the repository root, named in lowercase with no spaces so the URL stays clean (`python.html`).
- Add a card for it to `index.html`, with a title and a one-line description.
- Set `lang="en-CA"` on `<html>` and give the page a `<title>`. CI checks both, that every link resolves, and that each poster has a card on the landing page.

## Deployment

Pushing to `main` runs `.github/workflows/deploy-pages.yml`, which validates the repository and then publishes the repository root to GitHub Pages with `actions/deploy-pages`.
