# quarto-thesis

Quarto extension for a masters or PhD thesis based on Masters/Doctoral Thesis, LaTeX Template, Version 2.5 (27 Aug 2017). You can play with it on RStudio Cloud without installing anything: https://rstudio.cloud/content/4383755  Go to the Build tab (upper right panel) and click Render Book.

## Quick Start!

Show me how to download a zip and open in RStudio: [Video](https://youtu.be/33l8GhtUfnU)


## Installing the extension

You will need to do this to get all the folders with tex files.

```bash
quarto use template nmfs-opensci/quarto-thesis
```

Once you do that you can render from within the folder.

```bash
quarto render
```

## Installation or updating for an existing document

You may also use this format with an existing Quarto project or document. But you will need to have all the tex folders already (see above).

```bash
quarto install extension nmfs-opensci/quarto-thesis
```

## Usage

Start adding Chapters to the Chapters folder.

## Getting and giving help

First try the Discussion link because there may be a solution there. Have a solution to post or want to show how you have used this template? Post to the discussion forum too! You'll find links to other Quarto thesis templates there too.

If you think it's a bug, then definitely post an issue and I'll look into it! 

## Contributors

[![Contributors](https://contrib.rocks/image?repo=nmfs-opensci/quarto-thesis)](https://github.com/nmfs-opensci/quarto-thesis/graphs/contributors)

This template is based on the [Masters/Doctoral Thesis, LaTeX Template, Version 2.5 (27 Aug 2017)](https://www.latextemplates.com/template/masters-doctoral-thesis). Other Quarto thesis examples:


## Problems

* All the stuff in Frontmatter is mandatory LaTeX since it is being injected into the tex document after the qmd is processed. Probably need to learn how to write a lua filter to render the Frontmatter qmd to LaTeX via Pandoc.

* I doubt that passing in `classoptions` in your `_quarto.yml` will work. The [elsevier lua filter](https://github.com/quarto-journals/elsevier/blob/main/_extensions/elsevier/elsevier.lua) suggests that the classoptions need to be added on.

* Why does `index-blx.bib` keep appearing?

## Warning. Chapter 1 has R code

Python and Julia users: After you install the extension, search for `{r}` in `Chapters/Chapter1.qmd` and get rid of the R code (for a table and a figure) or replace with Python or Julia code.
