# Abigail Whalen — personal website

A small Jekyll site with three pages: About Me (the home page), CV, and Contact Me.
Pushing to `main` builds and publishes the site automatically via GitHub Actions.

## Editing content

The three pages live in `_pages/` as Markdown files:

| Page       | File                  | Address    |
| ---------- | --------------------- | ---------- |
| About Me   | `_pages/about.md`     | `/`        |
| CV         | `_pages/cv.md`        | `/cv/`     |
| Contact Me | `_pages/contact.md`   | `/contact/`|

Edit the text below the `---` block at the top of each file and commit. Site-wide
settings — the title, the sidebar name, bio, location, email, and academic profile
links — are in `_config.yml`. The header menu is in `_data/navigation.yml`.

## Adding the CV

The CV page links to `files/cv.pdf`, which does not exist yet. Add the PDF at that
exact path (`files/cv.pdf`) and commit it; the download link will start working.
To use a different filename, update the link in `_pages/cv.md` to match.

## Adding a profile photo

Put the image in `images/` and set `author.avatar` in `_config.yml` to the filename,
for example `avatar: "profile.jpg"`. Leaving it blank hides the avatar entirely.

## Publishing

Every push to `main` triggers `.github/workflows/deploy.yml`, which builds the site
and deploys it to GitHub Pages. One-time setup, in the repository's
**Settings → Pages**: set **Source** to **GitHub Actions**.

## Previewing locally

Requires Ruby 3.x.

```bash
bundle install
bundle exec jekyll serve
```

The preview is served at <http://localhost:4000>.
