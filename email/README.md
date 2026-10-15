# Email newsletter stuff

`template.heml` uses the HEML templating language for HTML email. Normally
there's a `heml` CLI tool, part of the npm `heml` package. We use our own
`./custom_heml`, which contains some extra CSS processing (expanding CSS vars).

To work on the template:

```
./custom_heml develop template.heml --open
```

To compile it and copy-paste it as a template into Listmonk:

```
./custom_heml compile template.heml
```

This creates `template.html`, the `{{ template "content" . }}` placeholder is
replaced by listmonk.

Individual newsletters are written here as `.md` files. `compile_email_md` turns
them into HTML, inserts it into the template, compiles the whole thing with
HEML, then extracts just the content, and writes it out as HTML (with lost of
inline styles). Copy-paste this as a post in Listmonk, using the template.
