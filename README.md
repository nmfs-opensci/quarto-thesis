# quarto-thesis

Quarto extension for a masters or PhD thesis based on Masters/Doctoral Thesis, LaTeX Template, Version 2.5 (27 Aug 2017)


## Installing the extension

You will need to do this to get all the folders with tex files.

```bash
quarto use template nmfs-opensci/quarto-thesis
```

## Installation for an existing document

You may also use this format with an existing Quarto project or document. But you will need to have all the tex folders already.

```bash
quarto install extension nmfs-opensci/quarto-thesis
```


## Usage

Start adding Chapters to the Chapters folder.

## Problems

* Meh, all the stuff in Frontmatter is mandatory LaTeX since it is being injected into the tex document after the qmd is processed. Probably need to learn how to write a lua filter to render the Frontmatter qmd to LaTeX via Pandoc.

* I doubt that passing in `classoptions` in your `_quarto.yml` will work. The [elsevier lua filter](https://github.com/quarto-journals/elsevier/blob/main/_extensions/elsevier/elsevier.lua) suggests that the classoptions need to be added on.

