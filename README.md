# LaTeX
A collection of frequently used styles for University of Latvia academic works. Assumes Latvian as the primary
language and English as the secondary.

## Dependencies
* Properly configured XeLaTeX environment. On Arch Linux `texlive-core`, `texlive-bin` and `biber` should be sufficient.
  Haven't tested it but `texlive-latexextra` and `texlive-bibtexextra` might be required as well.
* [biblatex-ieee](https://github.com/josephwright/biblatex-ieee) package.
* [fixlatvian.sty](https://github.com/andreyv/fixlatvian).
* [tikzit.sty](https://github.com/tikzit/tikzit/blob/master/tex/sample/tikzit.sty) package.

## Installation
On Linux systems just drop the `texmf` folder in you home folder. You might be required to run `texhash`
in order for LaTeX to find the newly installed packages. After that you can include the required packages in your
document, for example, `\usepackage{LU}`. A typical preamble would look like this:
```latex
\documentclass[a4paper,12pt]{article}

\usepackage{LU}
\usepackage{latex_article}
```

I'd suggest using `latexmk` to compile the document.
[Here's an example latexmk configration file](https://github.com/rhssk/dotfiles/blob/master/.latexmkrc).
