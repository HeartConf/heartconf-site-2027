# HeartConf 2027 site

HeartConf site, served through Github pages ([2027.heartconf.eu](https://2027.heartconf.eu)).

This site is built with Jekyll (static site generator supported by Github
pages), which requires Ruby.

To install Jekyll and dependencies, run `bundle install` in this repo.

To serve the site locally, for development, run:

```
bundle exec jekyll serve
```

The site is served at [http://localhost:4000](http://localhost:4000)

## Directory layout

Files included in the root that don't start with `_` or `.` are copied verbatim,
so any static assets are simply added to the root.

- `favicon.ico`
- `css/*`
- `images/*`

Markdown files are converted to HTML, they get a YAML "preamble" that indicates
the HTML layout to use, the page title, and the URL slug (`permalink`) the
page will appear at (this should generally follow the file name and directory
structure).

Page layouts go in `_layouts`, and reusable building blocks go under `_includes`. Both use the [Liquid](https://jekyllrb.com/docs/liquid/) templating language.

- `{{ variable }}`
- `{% include some_include.html %}`
- `{% if condition %} ... {% else %} ... {% endif %}`
