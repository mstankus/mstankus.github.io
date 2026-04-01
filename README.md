# mstankus.github.io template

This repository layout gives you:

- a custom landing page at the site root
- multiple mdBook sites under subpaths
- a GitHub Actions workflow that deploys the assembled static site to GitHub Pages

## Repository layout

```text
.
├── .github/workflows/deploy.yml
├── assets/site.css
├── index.html
├── proofs-and-structures/
└── rust-fundamentals/
```

## Expected repository name

For a personal GitHub Pages site, the repository should be named:

```text
mstankus.github.io
```

## How deployment works

The workflow:

1. installs mdBook
2. copies `index.html` and `assets/site.css` into `_site/`
3. builds each mdBook into a subfolder of `_site/`
4. deploys `_site/` to GitHub Pages

## First-time setup on GitHub

1. Create or reuse the repository `mstankus.github.io`.
2. Replace the contents with the files in this template.
3. Push to the `main` branch.
4. In GitHub, open **Settings -> Pages**.
5. Ensure the site is configured to use **GitHub Actions** as the source.
6. Wait for the workflow to complete.

## Local preview

Install mdBook, then run:

```bash
mdbook serve rust-fundamentals --open
mdbook serve proofs-and-structures --open
```

The landing page is plain HTML, so you can preview it with any static file server.

## Replacing placeholder content

- Edit `index.html` to change the cards and top-level branding.
- Replace the Markdown files in each `src/` directory.
- Add more books by copying one of the existing book directories and linking it from `index.html`.
