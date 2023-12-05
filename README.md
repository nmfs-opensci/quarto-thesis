[![github](https://img.shields.io/github/v/release/nmfs-opensci/quarto-thesis?color=brightgreen&label=GitHub)](https://github.com/nmfs-opensci/quarto-thesis/releases/latest)

# quarto-thesis

Quarto extension for a masters or PhD thesis based on Masters/Doctoral Thesis, LaTeX Template, Version 2.5 (27 Aug 2017). You can play with it on RStudio Cloud without installing anything: https://rstudio.cloud/content/4383755  Go to the Build tab (upper right panel) and click Render Book.

## Quick Start!

* Show me how to download a zip and open in RStudio: [Video](https://youtu.be/33l8GhtUfnU)
* Show me how to use this repo as a template and then clone to my computer with RStudio: [Video](https://youtu.be/smzNQtogSaI)
* Show me how to render in Visual Studio Code (see previous videos for how to get the repo onto your computer): [Video](https://youtu.be/IJe3A8-Ee2E)
* Scroll to the bottom for information on customizing the look of your thesis.


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

### Customizing the look

For a LaTeX document, the class file `MasterDoctoralThesis.cls` in the `_extensions/quarto-thesis` determines the look and LaTeX environments available. To make any changes to the layout, change the MasterDoctoralThesis.cls **in the _extensions folder**. The `MastersDoctoralThesis.cls` file in the main folder will be overwritten by the one in the `_extensions` folder when you re-rerender.  To get info on the MasterDoctoralThesis document class, do a web search for `MasterDoctoralThesis.cls`. You'll find some documentation.

### Adding content

* start adding Chapters in qmd format to the Chapters folder.
* then add the chapter (or appendix) to the `_quarto.yml` file

<img width="305" alt="image" src="https://github.com/nmfs-opensci/quarto-thesis/assets/2545978/3cbd21f5-185f-4930-8699-a623af15fd84">


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
