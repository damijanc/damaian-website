# damaian-site

Landing page for [Damaian](https://github.com/damijanc/damaian), built with Jekyll.

## Run locally

```sh
bundle install
bundle exec jekyll serve      # http://localhost:4000
```

## Build for hosting

```sh
JEKYLL_ENV=production bundle exec jekyll build   # output in _site/
```

`_site/` is plain static files. Copy it to any web server (nginx, Caddy, S3, GitHub Pages).
See `nginx.conf.example` for a minimal nginx server block.

Before deploying, set `url` (and `baseurl` if you serve from a sub-path) in `_config.yml`.

## Editing content

| What | Where |
|---|---|
| Name, tagline, all links | `_config.yml` |
| Feature list | `_data/features.yml` |
| FAQ | `_data/faq.yml` |
| Page sections | `index.html` |
| App illustration | `_includes/app-mock.html` |
| Styles | `assets/css/main.css` (tokens copied from the app's `docs/UI_STYLE_GUIDE.md`) |

Restart `jekyll serve` after changing `_config.yml`; other files reload automatically.
