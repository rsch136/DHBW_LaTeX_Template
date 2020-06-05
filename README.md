# LaTeX-Template for Project- and Bachelorthesis at DHBW Mannheim

This GitHub repository provides instructions, best practices, and a template for writing a project or bachelor thesis at the Department of Business Informatics at DHBW Mannheim.

## General Notes
* __The template is just a sample!__ Please adapt it to the requirements of your scientific advisor (i.e. adapt citation style, page margins etc.)
* __Always use the latest version of this template!__
* The template is written for a thesis in German, but can be adapted easily to other languages.
* **Using this template requires basic knowledge of LaTeX! Please get used to it *before* you start writing!**
* If you prefer to work with other text processing tools, you may nonetheless use **`master.pdf`** as guideline for the general sttructure of your project of bachelor thesis.
* [Here](hinweise-wissenschaftliche-arbeiten.md) are some general remarks (in German) on how to write scientific your thesises.


## Installation Instructions

### Prerequisites

First, you'll need a working LaTeX installation. Please find one for your
operating system, e.g.:

* Windows, Mac and Linux Users: [TexLive](http://www.tug.org/texlive/) (included in most Linux distributions)
* Windows Users: [MikTex](http://www.miktex.org)
* Mac Users: [MacTex](http://www.tug.org/mactex/index.html)

Next, you'll need a LaTeX Editor you're comfortable with. Any text editor (e.g. vi/vim, atom, sublime etc.) will do the job. Here are two specialized LaTeX editors tested with the template:

* [TexStudio](http://www.texstudio.org) (Platform-Independent)
* [TexShop](http://pages.uoregon.edu/koch/texshop/) (Mac only)

### Template Installation

Clone/download the template to your machine and unpack it to a directory of your choice (in case of zip download).

The template itself is pure LaTeX with only four template-specific commands which are _not_ LaTeX Standard [(see below)](#markdown-header-template-specific-commands).

The template files are commented quite well and it also includes an instruction chapter which explains the basic usage of the template (actually, the instruction chapter is in German).

Citation examples are included in the **`bibliography.bib`** file (articles, books, online references, etc.).

**Important:** Instead of BibTeX, the template uses the newer BibLaTeX/Biber combination. Please adjust your LaTeX environment accordingly when you get strange errors referring to the bibliography, since most editors default to BibTeX.

## Explanation of the template
The file **`master.tex`** is the TeX root file which can be compiled directly. All other `.tex`-Files are incuded from here. Read the comments in the file carefully, since you'll likely need some modifications here (e.g. for disabling unused stuff like the *List of Algorithms* etc.).

The file **`config.tex`** includes relevant packages and does some configuration stuff. Nearly every property or characteristic can be configured/modified here, beginning from page layout, header and footer, citaion style etc.). *Please also read the comments in the file catefully and - if needed - read the package documentations at [CTAN](http://www.ctan.org)!*

In particular adapt in master.tex and config.tex all parts which are marked with **`@stud`**.

Lists of figures, tables, coding sections, algorithms will be generated automaticvally during LaTeX compilation if these items are properly captioned -- see LaTeX instructions for details. Acronyms will be maintained in file **`acronyms.tex`**. The acronyms list will then also be generated automatically upon compilation with LaTeX.

The package contains sample chapter and appendix files which may be adapted and extended. Additional chapter and appendix files need to be included in the `master.tex` file.

If you want to use a logo of your company replace the graphics file **`firmenlogo.jpg`** in folder `./img` by the logo of your company. Adjust the size of the logo by setting the scale factor of the image in **`titlepage.tex`**.
