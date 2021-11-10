# jupyter-book-template

<a href="https://github.com/astro-group-bristol/jupyter-book-template/actions/workflows/gh_publish.yml">
<img alt="Publish" src="https://github.com/astro-group-bristol/jupyter-book-template/actions/workflows/gh_publish.yml/badge.svg"/>
</a>

<a href="https://astro-group-bristol.github.io/jupyter-book-template/">
<img alt="Docs" src="https://img.shields.io/badge/docs-dev-blue.svg"/>
</a>

*A template Jupyter Book for creating publication quality books from Jupyter Notebooks, markdown files, and more.*

## What does the template include?

This template is a minimally configured, custom styled [Jupyter Book](https://jupyterbook.org/intro.html), containing some information on how to get started with creating your own publication quality book. 

The repository is ready to be cloned for custom use, and has a generic Workflow configured to automatically rebuild and publish your book using GitHub Pages (may require setup if not used before).


## How do I use it?

Clone the repository, and setup a Python environment:


- using `pipenv` (recommended)

```bash
pipenv install 
```

- using `venv`

```bash
python3 -m venv .venv && source .venv/bin/activate

pip3 install -r requirements.txt
```

Then

1. Start by removing the `src/chapter*` directories.
2. Add your own content in a directory structure of your choosing.
3. Link all of the content you wish to include in the book in `src/_toc.yml`.
4. Update `src/_config.yml` as needed.

### Building and serving locally

Once you are happy with your content, you can build the book:

- using `pipenv` (recommended)

```bash
pipenv run build 
```

and serve locally with
```bash
pipenv run serve 
```

- using `venv`

```bash
jupyter-book build src
```
and serve it locally with 
```bash
python3 -m http.server -d src/_build/html
```

## Publishing your book

The Workflow file included will automatically rebuild and copy the `src/_build/html` directory to a new GitHub Pages branch.

If you wish to host the website elsewhere, only a file server is required (e.g. `/home/WWW/` on the Bristol servers). To do this, just copy the `src/_build/html` to the desired location, and point your a web browser there.