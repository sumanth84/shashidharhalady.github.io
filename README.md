# shashidharhalady.github.io

Personal articles site, published free via GitHub Pages. Supports English
and Kannada (ಕನ್ನಡ) articles side by side.

Live at: https://shashidharhalady.github.io

## Adding a new article

1. Create a new file in `docs/_posts/` named:

   ```
   YYYY-MM-DD-a-short-title.md
   ```

2. Add front matter at the top, then write the article body in Markdown
   below it:

   ```markdown
   ---
   title: "Your Article Title"
   date: 2026-09-28
   lang: en   # use "kn" for a Kannada article
   ---

   Your article content goes here, in Markdown.
   ```

3. Commit and push the file (or add it via the GitHub web UI's
   "Add file" button, which also works for typing Kannada text).

That's it — GitHub Pages rebuilds the site automatically within about a
minute of the push, no manual deploy step required.

## Local preview (optional)

```
cd docs
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Notes

- `lang: en` / `lang: kn` in an article's front matter controls the
  `lang` attribute used for that page and which font stack is applied
  (Kannada articles get the Noto Sans Kannada webfont automatically).
- The site uses GitHub Pages' built-in Jekyll build — no CI/CD setup or
  paid hosting is required.
