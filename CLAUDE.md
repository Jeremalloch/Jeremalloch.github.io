# Commands for al-folio Jekyll Site

## Build & Development

- Build site: `bundle exec jekyll build`
- Serve locally: `bundle exec jekyll serve --livereload`
- Deploy to GitHub Pages: `bin/deploy`
- Check site locally: `bundle exec jekyll serve --watch --port=8080 --host=0.0.0.0 --livereload`

## Testing & Validation

- Validate HTML: `bundle exec htmlproofer ./_site --disable-external`
- Check for broken links: `bundle exec htmlproofer ./_site --only-4xx --check-html`
- Format code: `npx prettier --write .`

## Code Style Guidelines

- Use 2-space indentation for all files (YAML, Markdown, Liquid, HTML)
- Follow Jekyll's naming conventions: lowercase with hyphens for files
- YAML front matter must be at the top of all content files
- Use relative URLs for internal links
- Image paths should be relative to site root
- Follow BEM methodology for CSS class naming
- Liquid tags should have spaces inside: `{% tag %}` not `{%tag%}`
- Keep markup semantic and accessible
- CV data should follow existing format in \_data/cv.yml
