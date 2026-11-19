# Department of Physics: research site

Source for **https://maynooth-physics.github.io**, built with [Quarto](https://quarto.org).
Every push to `main` rebuilds and publishes the site automatically (see `.github/workflows/publish.yml`).

## One-time setup

1. **Repo → Settings → Pages → Build and deployment → Source: GitHub Actions.**
2. **Allow the Quarto actions in the org:** Org Settings → Actions → General → "Allow … and select non-GitHub actions", then add:
   ```
   quarto-dev/*
   ```
   (Skip this step if the org already allows all actions.)
3. Push to `main`, then check the **Actions** tab. The first build takes about a minute.

## What to edit

| To change… | Edit |
|---|---|
| Home page text | `index.qmd` (the `.mu-hero` block and the contact band) |
| Research groups (cards on the home and Research Groups pages) | `groups.yml` |
| News | add a folder in `news/posts/`, copying the example one |
| About / Contact / Accessibility | `about.qmd`, `contact.qmd`, `accessibility.qmd` |
| Navbar and footer links | `_quarto.yml` |
| Colours and styling | `theme/mu.scss` (**this file is shared with the group sites**, see below) |

Search for `PLACEHOLDER` to find every piece of text you need to fill in.

## Adding a research group

1. Create the group's site from the **group-site-template** repo (see that repo's README).
2. Add a block for the group to `groups.yml`, with `path: https://maynooth-physics.github.io/<repo-name>/`.

## Preview locally (optional)

Install Quarto, then run `quarto preview` in this folder.

## Shared theme

`theme/mu.scss` and `assets/mu-logo-white.png` are also in every group site. When you change the
theme, copy the updated file into `theme/` in the template and in each group repo, so all the sites stay consistent.
