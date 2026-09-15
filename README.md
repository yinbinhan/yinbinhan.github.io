# yinbinhan.github.io

Personal academic website for Yinbin Han, served at <https://yinbinhan.github.io>.

Jekyll site built on [academicpages](https://github.com/academicpages/academicpages.github.io), itself a detached fork of the
[Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme (© 2016 Michael Rose, MIT — see LICENSE).
GitHub Pages rebuilds and deploys automatically on every push to `master`; there is no CI step and no manual build.

## Content

Editing these Markdown files is the whole maintenance workflow:

- `_pages/about.md` — bio and the News list (served at `/`)
- `_pages/research.md` — publication list, grouped into working papers, conference proceedings, and journal publications
- `_pages/teaching.md` — teaching assistant history
- `_pages/404.md` — not-found page
- `_config.yml` — site and `author:` metadata; `jekyll serve` does not reload this file, so restart the server after editing it
- `_data/navigation.yml` — top navigation
- `files/` — the CV PDF and anything else linked directly; published at `/files/<name>`

## Local preview

```
bundle install
bundle exec jekyll serve --livereload
```

Then open <http://localhost:4000>. Delete `Gemfile.lock` and retry if `bundle install` fails.

## Theme internals

`_sass/`, `_includes/`, `_layouts/`, and `assets/` are upstream theme code and are not edited as part of normal content
updates. `assets/js/main.min.js` is a build artifact — regenerate it with `npm install && npm run build:js` after changing
anything under `assets/js/`.
