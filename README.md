# roshanmsb.github.io

[![deploy](https://github.com/roshanmsb/roshanmsb.github.io/actions/workflows/deploy.yml/badge.svg)](https://github.com/roshanmsb/roshanmsb.github.io/actions/workflows/deploy.yml)

Source for the personal academic website of **Roshan Balaji**: PhD scholar and Prime Minister's Research Fellow at IIT Madras, working on machine learning for biology and chemistry.

**Live site:** https://roshanmsb.github.io

The site is built with [Jekyll](https://jekyllrb.com/) on the [al-folio](https://github.com/alshedivat/al-folio) theme.

## Updating content

| What | Where |
| --- | --- |
| Bio and home page | `_pages/about.md` |
| Publications | `_bibliography/papers.bib` (add `selected={true}` to show a paper on the home page) |
| News | `_news/announcement_N.md`: create the next-numbered file with a `date` in its front matter |
| CV page | `_data/cv.yml` |
| CV download | `assets/pdf/cv.pdf` |
| Site settings, social links, author highlighting | `_config.yml` |
| Co-author links / venue badges | `_data/coauthors.yml`, `_data/venues.yml` |
| GitHub repositories page | `_data/repositories.yml` |

To mark equal contribution in `papers.bib`, append `*` to the author's last name (e.g. `Balaji*, Roshan`) and add `note={* Equal contribution}`.

## Running locally

With Ruby and Bundler:

```bash
bundle install
bundle exec jekyll serve --port=8080 --livereload
```

Or with Docker:

```bash
docker-compose up
```

The site is served at http://localhost:8080.

## Deployment

Pushing to `master` triggers the GitHub Actions workflow in `.github/workflows/deploy.yml`. It builds the site and publishes it to the `gh-pages` branch, which GitHub Pages serves. Pull requests are built but not deployed.

## Credits

The theme is [al-folio](https://github.com/alshedivat/al-folio) by Maruan Al-Shedivat and contributors, released under the [MIT License](LICENSE). See the upstream repository for theme documentation and the FAQ.
