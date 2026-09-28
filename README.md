# shashidharhalady.github.io

Personal articles site, built with [Hugo](https://gohugo.io) and the
[PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, published
free via GitHub Pages. Supports English and Kannada (ಕನ್ನಡ) as separate
language sections, with a self-hosted Kannada webfont.

Live at: https://shashidharhalady.github.io

## Adding a new article

1. Create a new file in `content/en/posts/` (English) or
   `content/kn/posts/` (Kannada) named:

   ```
   YYYY-MM-DD-a-short-title.md
   ```

2. Add front matter at the top, then write the article body in Markdown
   below it:

   ```markdown
   ---
   title: "Your Article Title"
   date: 2026-09-28
   tags: ["tag-one"]
   ---

   Your article content goes here, in Markdown.
   ```

3. Commit and push the file (or add it via the GitHub web UI's
   "Add file" button, which also works for typing Kannada text).

That's it — a GitHub Actions workflow (`.github/workflows/hugo.yml`)
rebuilds and republishes the site automatically within about a minute of
the push, no manual deploy step required.

**One-time setup**: this repo's GitHub Pages source must be set to
**GitHub Actions** (Settings → Pages → Build and deployment → Source),
not "Deploy from a branch", for the workflow to publish successfully.

## Local preview (optional)

```
hugo server -D
```

Then open http://localhost:1313.

## Site structure

```
hugo.yaml                    Site config, including per-language menus
content/en/                  English pages and posts
content/kn/                  Kannada pages and posts
assets/css/extended/         Custom CSS (loaded automatically by PaperMod)
static/fonts/                Self-hosted Noto Sans Kannada (.woff2)
themes/PaperMod/             Theme, as a git submodule
```

## Notes

- The site is split into two independent language sections — English at
  `/` and Kannada at `/kn/` — each with its own nav menu, About, and
  Awards pages, switchable via the language link in the header.
- Kannada text uses a self-hosted Noto Sans Kannada webfont
  (`static/fonts/`, declared in `assets/css/extended/custom.css`), so it
  renders correctly without depending on Google Fonts or the visitor's
  OS having a Kannada font installed.
- The theme is a git submodule. If you clone this repo fresh, run
  `git submodule update --init --recursive` before building locally.
