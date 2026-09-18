# AGENTS.md

Read `README.md` first.

## Repository Guidance

- This is a static GitHub Pages site rooted at `index.html`. There is nothing to build, install, or bundle.
- Each poster is one self-contained HTML file at the repository root, with its CSS and JavaScript inline. No external scripts, stylesheets, fonts, or images.
- `index.html` defines the shared look: the `:root` colour variables, the `prefers-color-scheme: dark` override, the `--sans`/`--mono` font stacks, and the card styling. Posters repeat those variables rather than importing them, so keep the values in step.
- Posters carry their own `@media print` rules; a change to a poster's layout needs checking in print preview as well as on screen.
- A script in `<head>` colours the Python in each `<pre>` when the page loads, using the `--kw`, `--str`, `--num`, `--fn`, and `--bi` token colours. It skips `<i>` elements, so comments stay marked by hand as `<i># ...</i>` and remain muted without JavaScript. A poster in another language needs its own keyword and builtin lists.
- Canadian spelling throughout.

## Commands

There is no local toolchain. To check the site, open `index.html` in a browser. To run the checks CI runs, read `.github/workflows/test.yml`.

## Dependency Policy

The only dependencies are the GitHub Actions used by the workflows, pinned to major version tags. Dependabot handles upgrades.
