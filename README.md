University of Magallanes Thesis Rmarkdown Template
========================

This repository provides a template for a University of Sydney Honour/Master/PhD thesis using Rmarkdown with the `bookdown` R-package. This template is largely adapted from [unofficial University of Toronto R Markdown thesis template](https://www.sgs.utoronto.ca/academic-progress/program-completion/formatting/) developed and maintained by Francois Pitt. It is modified to prepared Thesis of Mauricio Mardones in Antarctic andSubAntarctic Sciene doctoral Program in University of Magallanes.

## Difference to Toronto Thesis

At this present moment, the difference is minor. The major difference lies in the ability to customise the School/Department, University, Country, logo and some metadata of the pdf (subject and keyowrds) from the YAML of `index.Rmd`. and addingdirector and codirectors

## Requirements

You will need to install the `bookdown` R package.

```r
install.packages('bookdown')
```

You will also need LaTeX installed. If you don't already have LaTeX, you can install [here](https://www.latex-project.org/get/) or use R:

```r
install.packages('tinytex')
tinytex::install_tinytex()
```

## Editor

It is preferred that you use [RStudio](https://www.rstudio.com/) for editing or [Sublime](https://www.sublimetext.com).

## Getting Started

Once you download the template, either open the `myThesis.Rproj` or go to the directory of the thesis folder. To compile the book run the following command at the console: 

```r
bookdown::render_book("index.Rmd", "bookdown::pdf_book")
``` 

The compiled thesis will be located in the folder `compiled_thesis`.

For customisation, modify the yaml of `index.Rmd` and `_bookdown.yml`. Notice that you can include chapters written in tex.  

to recompile a render it is necessary to delete the `thesisDOCAS.RMD` file

