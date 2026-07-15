# sina-HSA.github.io

Personal academic website of Sina Darabi, built with the
[Academic Pages](https://github.com/academicpages/academicpages.github.io) template
(a fork of [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)) and hosted
on GitHub Pages at <https://sina-hsa.github.io>.

## Where the content lives

| What | File |
| --- | --- |
| Site title, sidebar, links | `_config.yml` |
| Header menu | `_data/navigation.yml` |
| Front page (bio, news) | `_pages/about.md` |
| CV page | `_pages/cv.md` |
| One file per paper | `_publications/YYYY-MM-DD-slug.md` |
| One file per course | `_teaching/YYYY-MM-DD-slug.md` |
| PDFs, BibTeX | `files/` |
| Photos | `images/` |

## Adding a paper

Create `_publications/2027-06-01-short-name.md`:

```yaml
---
title: "Full title of the paper"
collection: publications
category: conferences        # conferences | manuscripts | workshops | patents
permalink: /publication/2027-06-01-short-name
date: 2027-06-01
venue: 'Name of the conference or journal'
citation: 'S. Darabi, and A. Coauthor. (2027). &quot;Title.&quot; <i>Venue</i>. pp. 1-12.'
paperurl: '/files/short-name.pdf'      # optional
slidesurl: '/files/short-name-slides.pdf'  # optional
bibtexurl: '/files/papers.bib'         # optional
---

Optional abstract or notes, in Markdown.
```

The date controls sort order and the URL; the year shown on the page comes from it.
Category headings are defined under `publication_category` in `_config.yml`.

## Still to do

- Replace `images/profile.png` with a real photo (square, ~400×400).
- Add `paperurl:` links — no PDF or DOI links were in the CV, so no paper currently has one.
- Fill in coauthors for the papers listed as "et al." (Lazy-LLC, Morpheus, OSM, and the TACO paper).
- Confirm the contact email; `darabs@usi.ch` is from the CV, but a BSC address may be better now.

## Running locally (optional)

```bash
bundle install
bundle exec jekyll serve -l -H localhost
```

Then open <http://localhost:4000>. This is only needed to preview before pushing —
GitHub builds the site automatically on every push to `main`.
