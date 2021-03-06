[![Build Status](https://travis-ci.org/quantum-journal/quantum-journal.svg?branch=master)](https://travis-ci.org/quantum-journal/quantum-journal)

# LaTeX document class for Quantum

`quantumarticle` is the document class for typsetting articles in Quantum.

[Click here](https://raw.githubusercontent.com/quantum-journal/quantum-journal/master/quantumarticle.cls) to download the latest stable version.

## Installation and usage

To use the `quantumarticle` document class with LaTeX simply start your document with the line:

```latex
\documentclass[your options]{quantumarticle}

```
Before you can do this however, you must make `quantumarticle.cls` accessible to your LaTeX compiler. You have several options for doing this:

1. The `quantumarticle` class is provided with install scripts for bash and PowerShell. These scripts should work for Windows 7 or later with MiKTeX, or for TeX Live with Linux or macOS / OS X. To install the class into your user-local LaTeX directory you would first clone this git repository `git clone https://github.com/quantum-journal/quantum-journal.git quantum-journal` and them from within bash execute:
 ```bash
 $ cd quantum-journal/
 $ ./install.sh
 ```
 Similarly, under PowerShell:
 ```powershell
 PS > cd quantum-journal/
 PS > ./install.ps1
 ```

2. Alternatively you can use `quantumarticle.cls` without installing it by simply downloading it directly via [this link](https://raw.githubusercontent.com/quantum-journal/quantum-journal/master/quantumarticle.cls) and putting it in the same folder as your main LaTeX source file. This can be the most convenient option if you are working on a manuscript together with collaborators that do not want to install `quantumarticle.cls` and are exchanging the source files of your manuscript via email or cloud storage services. When you upload your manuscript to the arXiv you will anyway have to include `quantumarticle.cls` along with other source files.

3. To manually install `quantumarticle`, you can either clone this git repository or download `quantumarticle.cls` directly via [this link](https://raw.githubusercontent.com/quantum-journal/quantum-journal/master/quantumarticle.cls) and then copy the `quantumarticle.cls` file to `texmf/tex/latex/quantumarticle` within your home directory (under Linux, macOS, and OS X `~/`, or under Windows typically `C:\Users\[your username]`) and run `texhash` (TeX Live) or `initexmf --update-fndb` (MiKTeX).

4. Finally, you can use `quantumarticle.cls` without even downloading it at all on the collaborative writing platform [overleaf](https://www.overleaf.com/) by starting your project from the `quantumarticle` [template](https://www.overleaf.com/latex/templates/template-for-submission-to-quantum-journal/gsjgyhxrtrzy) as well as with the [ShareLaTeX](https://www.sharelatex.com/project) online LaTeX editor by using the `quantumarticle` [template](https://www.sharelatex.com/templates/5912bce26aad110026f11697) there.

## Dependencies

`quantumarticle.cls` should work with any reasonably recent LaTeX distribution. It further requires the following packages: `xkeyval`, `etoolbox`, `geometry`, `xcolor`, `fancyhdr`, `tikz`, `hyperref`, ltxgrid and ltxcmds (often distributed along with revtex, in texlive for example as part of `texlive-publishers`), as well as at least either `lmodern` or `type1ec`. We recommend to have `natbib` and at least one of `bbm` or `dsfont` installed. All of these should be included in the full install variant of your LaTeX distribution (for example `texlive-full`).

## Compatibility

The `quantumarticle` class tries to be **maximally compatible** with existing document classes, such as, `article`, `revtex`, `iopart`, and `elsarticle`. It supports all standard options, like `twocolumn`, `onecolumn`, `titlepage`, as well as the standard syntax for defining the title page with the `\author`, `\address`, and `\affiliation` commands and the `abstract` environment.

## Contributing

In case you encounter problems using the article class please consider opening a bug report in our [bug-tracker on github](https://github.com/cgogolin/quantum-journal/issues).
You can also contact us via email under latex@quantum-journal.org, but it may take significantly longer to get a response.
In any case we need the full source of a document that produces the problem and the log file showing the error to help you.

Improvements submitted as pull requests against the `development` branch are very much appreciated!

## Copyright

Copyright 2017
Verein zur Förderung des Open Access Publizierens in den Quantenwissenschaften
(http://quantum-journal.org/about/)

`quantumarticle.cls` is derived from `article.cls` available from
https://www.ctan.org/pkg/article

It may be distributed and/or modified under the
conditions of the LaTeX Project Public License, either version 1.3c
of this license or (at your option) any later version.
The latest version of this license is in
http://www.latex-project.org/lppl.txt
and version 1.3c or later is part of all distributions of LaTeX
version 2005/12/01 or later.
