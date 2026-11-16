# Kirishana Kiritharan — Portfolio

A responsive, static portfolio site built with HTML and CSS. The website source is in
[`site/`](./site), separate from the source CV in `doc/`.

## GitHub Pages deployment

The workflow in [`.github/workflows/deploy-pages.yml`](./.github/workflows/deploy-pages.yml)
deploys the contents of `site/` to GitHub Pages after every push to `main`. It can also
be started manually from the repository’s **Actions** tab.

To publish the site:

1. Push this project to a GitHub repository using the `main` branch.
2. In the repository’s **Settings → Pages**, set the build and deployment source to
   **GitHub Actions** if it is not already selected.
3. Allow the workflow to run. The published URL will appear in the workflow run and
   the repository’s Pages settings.

Only `site/` is uploaded as the website artifact; the CV and other repository files
are not included in the deployed site.
