# Portfolio

A minimal Hugo site with plain HTML. No theme, CSS, JavaScript, npm, or custom Go server.

## Run

From this repository directory:

```sh
hugo server -D --baseURL http://localhost:1313/
```

Open http://localhost:1313/ and leave the terminal running. Stop with Ctrl+C.

## Files to edit

- `content/_index.md`: homepage introduction.
- `content/about.md`: biography.
- `content/projects/*.md`: project content. Each file begins with JSON metadata followed by Markdown. Copy one to add a new project; `weight` controls its position.
- `layouts/baseof.html`: shared HTML, navigation, and footer.
- `layouts/list.html`: homepage and project listing.
- `layouts/single.html`: individual pages.
- `hugo.toml`: site title and published URL.

The browser provides the default appearance. Build your own HTML structure in `layouts/`. When ready to style it, create `static/style.css` and link it in the shared template using Hugo's `relURL` helper.

## Build

```sh
hugo --minify
```

This generates `public/` for static hosting. `baseURL` is configured for https://yeababate.github.io/portfolio/; publication is separate.
