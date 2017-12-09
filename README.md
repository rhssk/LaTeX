# LaTeX
A collection of frequently used styles for University academic works

## Requirements
* Properly configured XeLaTeX environment. On Arch Linux `texlive-core`, `texlive-bin` should be sufficient. Haven't tested it
but `texlive-latexextra` and `texlive-bibtexextra` might be required as well.
* [fixlatvian](https://github.com/andreyv/fixlatvian) package by Andrey Vihrov. Provides punctuation rules for sections etc. This
is already included in this repo but you might want to check the original repo for updates, bug reports, feature requests etc.

## Installation
On Linux systems just drop the `texmf` folder in you home folder. You might be required to run `texhash` in order for LaTeX to find the newly installed packages.
After that you can include the required packages in your document, for example, `\usepackage{LU}`.
A typical preamble would look like this:
```latex
\documentclass[a4paper,12pt]{article}

\usepackage{fontspec}
\usepackage{polyglossia}
\setmainlanguage{latvian}
\usepackage{LU}
```

I'd suggest using `latexmk` to ease the compilation and linking process. [Here's an example latexmk configration file](https://github.com/rhssk/dotfiles/blob/master/.latexmkrc).

Also note that you might get a compilation error about biblatex not supporting latvian. Some text correctly falls back to translations
provided by polyglossia but you still might the occasional ugly `url:` etc. I'm currently working on translation for biblatex so hopefully that issue is solved soon.
