# Getting started with your own book

To use this template:

1. Start by removing the `src/chapter*` directories.
2. Add your own content in a directory structure of your choosing.
3. Link all of the content you wish to include in the book in `src/_toc.yml`, as described in {doc}`../chapter2/tocs`.
4. Update `src/_config.yml` as needed.
5. Build your book with

```bash
jupyter-book build src
```

and serve it locally with 
```bash
python3 -m http.server -d src/_build/html
```