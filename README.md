# UQ Open Science Rmarkdown

# What you need to do this course

1. R
    - Linux (https://cran.r-project.org/bin/linux/)
    - Mac OS (https://cran.r-project.org/bin/macosx/)
    - Windows (https://cran.r-project.org/bin/windows/base/)
1. RStudio - http://rstudio.com/products/rstudio/download
1. rmarkdown packages


```r
# install tinytex (for PDF documents)
install.packages('tinytex')
tinytex::install_tinytex()
```

# Points to cover

Here are some of the things that I want to cover today

- Basics of rmarkdown
- Keyboard shortcuts
- How to change the size and type of your figures
- Dynamically create tables of model output
- Refer to numbers from statistics in your text
- Add captions to tables and figures
- Cite tables and figures
- Cite R packages and change citation style:
- Understand the pros and cons of output formats
- Pros/cons of output formats - if you want flexibility (PDF or Word or HTML), you're limited in features; complex formulas, interactive graphics don't always translate
- Debug and handle common errors for rmarkdown
- The extendability of rmarkdown:
  - slides
  - books
  - websites
- Produce mathematical equations

# The breakdown

- Basics of rmarkdown
- Keyboard shortcuts
- Keep the output of document
- Customising output (figure size, etc)
- produce summary tables of your model
- produce inline content in your text:
- add captions to tables and figures
- cite tables and figures
- Globally change options for all code output:
- Cite packages and change citation style:
- Pros/cons of output formats - if you want flexibility (PDF or Word or HTML), you're limited in features; complex formulas, interactive graphics don't always translate
- Debug and handle common errors for rmarkdown
- The extendability of rmarkdown:
  - slides
  - books
  - websites
- Produce mathematical equations:

Here are the learning outcomes that we are working towards

Understand the basics of rmarkdown:

- Make a report with an introduction heading
- Add your name and date to the YAML header

Understand how to customise figure sizes and output:

- Change the fig.width, fig.height, and dev of the figure in plot-1
  - (hint: look at the gear icon in a chunk)
- print the code for one of the figures, but not the other (hint: use `echo = `)

Keep the output of figures and code:

- Add an option to keep the markdown source code 
  - (hint: look at the gear icon next to `knit` icon)

Produce mathematical equations:
  - Make an equation describing the relationship

produce summary tables of your model

  - fit a linear model of Ozone ~ Temp + Wind + Solar.R 
    - (hint: use `lm`)
  - Make a table of the coefficients from the linear model 
    - (hint: use `coef` and `knitr::kable`)
    
produce inline content in your text:

  - Make some inline code chunks that describe the single values of the R-squared or a coefficient

Globally change options for all code output:

- set a global option to: 
  - hide all of the code
    - hint: put `knitr::opts_chunk$set()` in a chunk and set the options
  - set the graphics device
    - hint: `dev = "png"` or even `dev = c("png", "pdf","tiff")`
  - set the DPI
    - hint: `dpi = 300`

Cite packages and change citation style:

- Cite the packages you use when you use them
  - hint: http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html
  - hint: look at the names in packages.bib
- Tidy up the structure, provide some more words around the introduction and results

Debug and handle common errors for rmarkdown

- Get this rmarkdown document to compile
  - hint:
    - knit the document and look at the line for the error
    - if there is an error:
       - recreate the session in an interactive session:
          - restart R
          - run all chunks below (top section Run>arrow>run all chunks below)
          - find the chunk that did not work, fix that chunk
          - run all chunks below (top section Run>arrow>run all chunks below)
          - explore working directory issues
            - where is the packages.bib file?
            - remember that the rmarkdown directory is where the .Rmd file lives
