# Nudibranch! News

A small static site for publishing discoveries and field notes about nudibranchs (sea slugs).

Logo mascot: the **Leopard Dorid**.

## Structure

```
.
├── index.html                                  # Homepage / list of stories
├── styles.css                                  # Site styles
├── articles/
│   └── striped-nudibranch-golden-gardens.html  # First article
├── images/                                     # Logo + photos (see images/README.md)
├── .nojekyll                                   # Serve plain HTML on GitHub Pages
└── .github/workflows/deploy.yml                # Deploys the site to GitHub Pages
```

## Adding the images

The site references three image files. See [`images/README.md`](images/README.md) for the
exact filenames to add.

## Publishing on GitHub Pages

This repository deploys automatically with GitHub Actions
(see [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)).

1. Push this branch and merge it into your default branch (`main`).
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Every push to `main` then builds and deploys the site automatically (you can also
   trigger it manually from the **Actions** tab). It will be published at
   `https://calysteon.github.io/nudibranch-news/`.

## Adding a new article

1. Copy `articles/striped-nudibranch-golden-gardens.html` as a starting template.
2. Update the title, dateline, headline, and body.
3. Add a new `<article class="story">` block to `index.html` linking to it.
