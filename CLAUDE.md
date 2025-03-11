# Commands for al-folio Jekyll Site

## Build & Development

- Build site: `bundle exec jekyll build`
- Serve locally: `bundle exec jekyll serve --livereload`
- Deploy to GitHub Pages: `bin/deploy`
- Check site locally: `bundle exec jekyll serve --watch --port=8080 --host=0.0.0.0 --livereload`

**IMPORTANT**: Do not run Jekyll serve commands when working with Jeremy as he's already running auto-rendering in another terminal.

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

## CV Content Management

- Two methods for CV content generation:
  1. Primary: JSON standard format in `assets/json/resume.json` (currently in use)
  2. Fallback: YAML format in `_data/cv.yml` (used when no resume data defined in \_config.yml)
- Jeremy has edited the resume.json file, which should be used by default
- When editing CV content, prioritize updates to the JSON format
- The YAML format is more human-readable but is not currently the primary source

## Screenshot References

- When Jeremy mentions taking a screenshot, check the most recent file in `~/Pictures/Screenshots/`
- Compare the timestamp of the screenshot with the current time using `date` and `ls -la`
- Flag if more than 5 minutes have elapsed between the screenshot timestamp and current time
- This helps identify situations where a screenshot may have failed to save or an old screenshot is being referenced
