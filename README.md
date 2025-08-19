<!--
worklog. last edit 2025-08-19 by jmill
- flesh out course-specific content and links
- scaffolded MkDocs + Material site, GH Pages workflow, docs for m01–m08
-->

# course companion (mkdocs + material)

lightweight site for written + visual content using Markdown. includes sidebar table of contents, modules m01–m08, and sample Streamlit embeds.

## features

- material theme with integrated sidebar ToC
- modules named `m01`..`m08` under `docs/modules/`
- supports iframe embeds (e.g., Streamlit)
- ready for GitHub Pages via Actions

## local dev

- install deps
  ```bash
  pip install -r requirements.txt
  ```
- run dev server (auto-reloads on save)
  ```bash
  mkdocs serve -a 127.0.0.1:8000
  ```
- open http://127.0.0.1:8000

## deploy (github pages)

- push to `main` (or `master`). action builds + deploys
- repo settings → Pages → Build and deployment: GitHub Actions
- site will publish at `https://<user>.github.io/<repo>/` (update `site_url` in `mkdocs.yml` when known)

## structure

```
.
├── mkdocs.yml
├── docs/
│   ├── index.md
│   ├── embeds.md
│   └── modules/
│       ├── m01.md
│       ├── m02.md
│       ├── m03.md
│       ├── m04.md
│       ├── m05.md
│       ├── m06.md
│       ├── m07.md
│       └── m08.md
└── .github/workflows/gh-pages.yml
```

## embed example (streamlit)

```html
<!-- optional: adjust height; use ?embed=true for Streamlit Cloud -->
<iframe src="https://<streamlit-app>.streamlit.app/?embed=true"
        width="100%" height="650" frameborder="0" allowfullscreen>
</iframe>
```

## notes

- keep file names lower-case; module files use `m##` naming
- prefer relative links (work with GitHub Pages subpath)
- use admonitions and tabs via pymdownx extensions
