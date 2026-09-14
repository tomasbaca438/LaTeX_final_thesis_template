# Thesis Template

## Project Information

- **Author:** Ing. Tomáš Bača
- **Faculty:** Faculty of Management Science and Informatics, University of Žilina
- **Version:** 1.0
- **License:** MIT License (see the `LICENSE` file)

Main LaTeX source template for a thesis. The document is compiled using **LuaLaTeX**, the text is typeset with the **Source Serif 4** font, and mathematical content uses **Cambria Math**. Bibliography management is handled by **Biber**.

---

# User Guide

## Requirements

- Compiler: **LuaLaTeX**
- Bibliography system: **Biber**

Recommended editor:

- **TeXStudio**: https://www.texstudio.org

---

## Perl Installation

**Perl** must be installed for **Biber** to work correctly.

Installation packages:

- https://www.perl.org/get.html

### Windows

Recommended distribution:

- Strawberry Perl

### Linux and macOS

Perl is usually installed by default as part of the operating system.

---

## LaTeX Distribution Installation

A LaTeX distribution provides:

- compilers,
- packages,
- dependency management,
- document creation tools.

Recommended distribution:

- **MiKTeX**: https://miktex.org

During installation, set:

```text
Install missing packages on-the-fly = Yes
```

---

## TeXStudio Configuration

Go to Options → Configure TeXstudio

Enable the following option in the settings:

```text
Show Advanced Options
```

Then navigate to:

```text
Build → Meta Commands → Build & View
```

and configure:

```text
txs:///lualatex |
txs:///biber |
txs:///makeglossaries |
txs:///lualatex |
txs:///lualatex |
txs:///view
```

Then navigate to:

```text
Build → Meta Commands → Default Compiler
```

and configure:

```text
LuaLaTex
```

Then navigate to:

```text
Build → Meta Commands → Default Viewer
```

and configure:

```text
PDF Viewer
```

Then navigate to:

```text
Build → Meta Commands → Default Bibliography Tool
```

and configure:

```text
Biber
```

---

# Thesis Configuration

## General Information

File:

```text
hlavicky/00_globalne_informacie_o_dokumente.tex
```

Contains:

- title page information,
- page header information,
- abstract header information.

---

## Thesis Assignment

Upload the assignment PDF file to:

```text
zadanie_prace/zadanie_prace.pdf
```

---

## Abbreviations, Symbols, and Terms

### Abbreviations

```text
hlavicky/00_skratky_defincie.tex
```

### Symbols

```text
hlavicky/00_symboly_definicie.tex
```

### Terms

```text
hlavicky/00_pojmy_definicie.tex
```

---

## Declaration, Acknowledgements, and Abstracts

File:

```text
hlavicky/00_informacie_cestne_vyhlasenie_podakovanie_abstrakt.tex
```

Contains:

- declaration of originality,
- acknowledgements,
- abstract in Slovak,
- abstract in English,
- keywords.

The content is automatically transferred to the corresponding pages.

---

## Thesis Chapters

General information and guidelines for writing the thesis can be found in:

```text
kapitoly/jadro.tex
kapitoly/spracovanie_zaverecnej_prace.tex
```

---

# Bibliography

Store all bibliography entries in:

```text
bibliografia/zaverecna_praca.bib
```

---

## Recommended Bibliography Management Tool

### JabRef

https://www.jabref.org/#download

It is recommended to run:

```text
Quality → Check Integrity
```

The `.bib` file should contain only the following warnings:

- `Journal not found in abbreviation list`
- `Citation key deviates from generated key`

---

## Formatting the .bib File

Recommended tool:

[https://flamingtempura.github.io/bibtex-tidy/](https://flamingtempura.github.io/bibtex-tidy/index.html?opt=%7B%22modify%22%3Atrue%2C%22omit%22%3A%5B%22abstract%22%5D%2C%22curly%22%3Atrue%2C%22numeric%22%3Atrue%2C%22months%22%3Atrue%2C%22space%22%3A2%2C%22tab%22%3Afalse%2C%22align%22%3A13%2C%22blankLines%22%3Atrue%2C%22duplicates%22%3A%5B%22key%22%2C%22doi%22%5D%2C%22stripEnclosingBraces%22%3Afalse%2C%22dropAllCaps%22%3Afalse%2C%22escape%22%3A%22new%22%2C%22unescape%22%3Afalse%2C%22sortFields%22%3A%5B%22title%22%2C%22shorttitle%22%2C%22author%22%2C%22year%22%2C%22month%22%2C%22day%22%2C%22journal%22%2C%22booktitle%22%2C%22location%22%2C%22on%22%2C%22publisher%22%2C%22address%22%2C%22series%22%2C%22volume%22%2C%22number%22%2C%22pages%22%2C%22doi%22%2C%22isbn%22%2C%22issn%22%2C%22url%22%2C%22urldate%22%2C%22copyright%22%2C%22category%22%2C%22note%22%2C%22metadata%22%5D%2C%22stripComments%22%3Atrue%2C%22trailingCommas%22%3Atrue%2C%22encodeUrls%22%3Atrue%2C%22tidyComments%22%3Atrue%2C%22removeEmptyFields%22%3Afalse%2C%22removeDuplicateFields%22%3Atrue%2C%22lowercase%22%3Atrue%2C%22backup%22%3Atrue%7D)

This tool automatically:

- sorts fields,
- removes duplicates,
- standardizes formatting,
- encodes URLs,
- adjusts indentation.

---

# Troubleshooting

If you encounter compilation problems:

1. Check the `.bib` file.
2. Remove problematic characters.
3. Remove HTML tags or invalid content.

Commonly problematic strings include:

```text
<a
</a>
href=
target=
rel=
class=
data-lexical
_

&
#
``
$
#:~:text=

<script
<div
<span
<strong
<i>
</i>
<b>
</b>
```

These characters and tags may cause issues during compilation with LuaLaTeX.

# Template in Slovak 

https://github.com/tomasbaca438/latex_sablona_zaverecnej_prace/blob/main/README.md
