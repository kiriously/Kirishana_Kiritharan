# Optimized Prompt: CV to Responsive Website (CRAFT method)

> **CRAFT** stands for **C**ontext, **R**ole, **A**ction, **F**ormat and **T**arget audience & Tone.

## C · Context

I have a CV stored in the `doc/` folder of this Git repository
(`doc/Kirishana_Kiritharan_CV.docx`). I am a Master's student in Healthcare Innovation
and Data Science at emlyon business school, with a Bachelor's in Data Science (ZHAW) and
professional experience at Siemens, Roche and EY.

I want to turn this CV into a modern, professional personal website that I can share with
recruiters and include in job applications. The repository is hosted on GitHub, and the
site must be published automatically with GitHub Pages.

Constraints:

* Static site only: **HTML and CSS** (minimal vanilla JavaScript only if truly needed). No frameworks and no build step.
* Keep the website source in a dedicated `site/` folder, separate from `doc/`.
* Only the website (not the CV file or other repository files) may be deployed.
* Do **not** publish private data from the CV: home address, phone number, and the
  names and email addresses of my references must stay off the website.

## R · Role

Act as a **senior front end developer and UX/UI designer** with experience in personal
branding and portfolio websites. You also know GitHub Actions and GitHub Pages well, follow
web accessibility best practice (WCAG 2.1 AA), and write clean, semantic, maintainable code.

## A · Action

Work through the following steps **in order**. Make **one Git commit per step**, with a
clear message in the Conventional Commits style (for example `feat: add experience section`).

1. **Analyse the CV.** Read the document in `doc/` and extract every section: profile
   summary, experience, projects, education, skills, languages and contact links. Report
   anything that is unclear or inconsistent before writing code.
2. **Ask clarifying questions** (see the list below) and wait for my answers before
   continuing.
3. **Set up the project.** Create `site/index.html` and `site/styles.css` with a semantic
   HTML5 structure (`header`, `nav`, `main`, `section`, `article`, `footer`) and SEO meta
   tags (title, description, viewport). Commit.
4. **Build the content sections:** introduction, profile, experience (timeline),
   projects (with the Bachelor's thesis featured), education, skills and languages, contact.
   Rewrite bullet points in a concise, professional tone focused on results, and keep all
   facts and figures exactly as stated in the CV. Commit after each major section.
5. **Apply responsive design.** Mobile first CSS using Flexbox and Grid, fluid typography
   (`clamp()`), and breakpoints for mobile (up to 680 px), tablet (up to 900 px) and desktop.
   No horizontal scrolling at a width of 360 px. Commit.
6. **Accessibility and polish.** Skip link, visible focus styles, sufficient colour
   contrast, ARIA labels where needed, and support for reduced motion. Commit.
7. **Automate deployment.** Add a GitHub Actions workflow in `.github/workflows/` that
   deploys `site/` to GitHub Pages on every push to `main` (and on manual
   `workflow_dispatch`), using the official GitHub Pages actions with least privilege
   permissions. Commit.
8. **Document.** Write a `README.md` explaining the project structure, how to preview the
   site locally, and how to enable GitHub Pages (Settings › Pages › Source: GitHub Actions). Commit.
9. **Verify.** Check that the HTML is valid, test at mobile and desktop widths, and confirm
   that the workflow runs successfully and the live URL works.

**Clarifying questions to ask me before building:**

* Which colour palette or visual style do you prefer (for example minimal, corporate or creative)?
* Should the site be in English only, or also in French or German?
* Which contact details may be public (email, LinkedIn)?
* Should visitors be able to download the CV as a PDF?
* Do you have a profile photo you want to include?
* Do you plan to use a custom domain?

**Writing rule:** do not use hyphens or dashes (no "-", "–" or "—") anywhere in the visible
website text or in the documentation. Rephrase instead, or use "·", "|" or "to" (for date
ranges such as "JUN 2025 to SEP 2026").

## F · Format

Deliverables:

```
.
├── .github/workflows/      # automatic GitHub Pages deployment
├── doc/                    # source CV (not deployed)
├── site/
│   ├── index.html          # single page website
│   └── styles.css          # all styles
├── PROMPT.md               # this prompt
└── README.md               # setup and deployment guide
```

For each step, reply with:

1. A short summary of what was done and why.
2. The files created or changed.
3. The Git commit message used.

At the end, provide the GitHub Pages URL and a short checklist of what was tested.

## T · Target audience & Tone

* **Website audience:** recruiters, hiring managers and academic contacts in data
  science, healthcare and consulting. They should understand my profile within
  30 seconds, on a phone or a laptop.
* **Website tone:** professional, clear and confident, using first or third person
  consistently. No slang or overly casual phrasing.
* **Design:** clean, modern and minimal, with plenty of white space, a restrained colour
  palette and readable typography.
* **Your communication with me:** clear and structured. If anything is ambiguous, ask
  rather than assume.
