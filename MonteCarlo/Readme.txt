
There are two types of output formats in the rmarkdown package: 
documents, and presentations. All available formats are listed below:

beamer_presentation
context_document
github_document
html_document
html_fragment
html_notebook
html_vignette
ioslides_presentation
latex_document
md_document
odt_document
pdf_document
powerpoint_presentation
rtf_document
slidy_presentation
word_document

There are more output formats provided in other extension packages (starting from Chapter 5). 
For the output format names in the YAML metadata of an Rmd file, 
you need to include the package name if a format is from an extension package, e.g.,

output: tufte::tufte_html

When you want to use certain options, you have to translate the values from R to YAML, e.g.,

html_document(toc = TRUE, toc_depth = 2, dev = 'svg')
can be written in YAML as:

output:
  html_document:
    toc: true
    toc_depth: 2
    dev: 'svg'
    
    
Look at themes at ?html_document_base {rmarkdown}

