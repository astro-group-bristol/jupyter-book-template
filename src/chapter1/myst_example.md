# MyST Markdown

For a comprehensive cheat sheet, see [the official documentation](https://jupyterbook.org/reference/cheatsheet.html).

Here is provided a short overview of some useful basics.

## Equations

You can write LaTeX equations either inline, such as $x^2 + y^2 = r^2$, or in display mode with

```{math}
:label: einstein_field_equation
G_{\mu\nu} + \Lambda g_{\mu\nu} = \frac{8 \pi G}{c^4} T_{\mu\nu}.
```

Note that either fenced sections (three back-ticks or `:::`) or double dollar signs (`$$`) can be used to denote display math. In the prior case, equations can be assigned a label with

```
:::{math}
:label: my_equation
:::
```

and referenced {eq}`einstein_field_equation`.

## Admonitions

Admonitions are richly formatted HTML objects, defined similarly to code blocks. To insert, for example, a note box into your content, you can use

````
```{note}
Here is a note
```
````

This results in:

```{note}
Here is a note
```

Alternatively, for a warning

````
```{warning}
Here is a dangerous warning.
```
````

This results in:

```{warning}
Here is a dangerous warning.
```

## Using roles

Roles are very similar to directives, but they are less-complex and written
entirely on one line. You can insert a role into your book's content with
this pattern:

```
Some content {rolename}`and here is my role's content!`
```

Again, roles will only work if `rolename` is a valid role's name. For example,
the `doc` role can be used to refer to another page in your book. You can
refer directly to another page by its relative path. For example, the
role syntax `` {doc}`intro` `` will result in: {doc}`intro`.

For more information on writing roles, see the
[MyST documentation](https://myst-parser.readthedocs.io/).


### Adding a citation

You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.

Moreover, you can insert a bibliography into your page with this syntax:
The `{bibliography}` directive must be used for all the `{cite}` roles to
render properly.
For example, if the references for your book are stored in `references.bib`,
then the bibliography is inserted with:

````
```{bibliography}
```
````

Resulting in a rendered bibliography that looks like:

```{bibliography}
```