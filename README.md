# Kirishana Kiritharan | Personal Website

A modern, responsive personal website based on my CV. It presents my profile, professional
experience, projects, education and contact details, and works on desktop, tablet and
mobile devices.

## Project structure

| Folder or file | Purpose |
| :--- | :--- |
| [`site/`](./site) | Website source: `index.html` (content) and `styles.css` (design) |
| [`doc/`](./doc) | Source CV in Word format (not published) |
| [`.github/workflows/`](./.github/workflows) | Automatic deployment to GitHub Pages |
| [`PROMPT.md`](./PROMPT.md) | The CRAFT prompt used to create the website |

## Features

* Single page layout with sections for profile, experience, projects, education and contact
* Responsive design built with CSS Grid, Flexbox and fluid typography
* Accessible markup: semantic HTML, skip link, visible focus styles and reduced motion support
* No frameworks and no build step: plain HTML and CSS only
* Private CV details (address, phone number, references) are not published

## Local preview

Open `site/index.html` directly in a browser, or start a small local server:

```bash
cd site
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deployment to GitHub Pages

The [deployment workflow](./.github/workflows/deploy-pages.yml) publishes the contents of
`site/` to GitHub Pages after every push to the `main` branch. It can also be started
manually from the **Actions** tab of the repository.

To publish the website:

1. Push this project to a GitHub repository on the `main` branch.
2. Open **Settings › Pages** and set the source to **GitHub Actions**.
3. Wait for the workflow to finish. The public URL is shown in the workflow run and in
   the Pages settings.

Only the `site/` folder is deployed. The CV and all other repository files remain private
to the repository.
