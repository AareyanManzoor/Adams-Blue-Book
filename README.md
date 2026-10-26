# Adams-Blue-Book
The TeX for Adams' blue book, by the group TeXromancers

The files are just as it was in our overleaf. This is a bit unorganized as it was our first project and we were figuring things out. 

Feel free to download and change for example font to better fit your preferences. Your can report errors to my email at amanzoo1 at asu dot edu, or at my discord JohnDS#1149, or as changes to this github with documentation of what was changed.

Here is a link to the book: https://people.math.rochester.edu/faculty/doug/otherpapers/Adams-SHGH-latex.pdf, thanks to Doug Ravenel for hosting this on his website!

Here is a link to the dyslexic friendly version: https://aareyanmanzoor.github.io/assets/blue-book-dyslexic.pdf .

## Source corrections

The 2026 correction pass compares this typesetting with the [1974 University of Chicago Press scan](https://www.sas.rochester.edu/mth/sites/doug-ravenel/otherpapers/Adams-SHGH-ocr.pdf). It restores omitted formulas and proof cases, repairs mathematical transcription and diagram errors throughout all three parts, and corrects chapter references and bibliography metadata. Mathematical errors inherited from the original are corrected with editorial notes, rather than silently reproduced. The preface to the new typesetting describes the editorial policy; intentional notation modernizations and the corrected cohomological AHSS coefficient `\pi_{-q}(F)` are retained.

## Building

Use a TeX distribution providing `latexmk`, pdfLaTeX, Biber compatible with the installed `biblatex`, and MakeIndex. From this repository's directory run:

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

The complete build must run Biber and MakeIndex and repeat LaTeX until citations, cross-references, and the index are resolved. The ordinary edition uses pdfLaTeX; enabling the optional dyslexic-font input requires LuaLaTeX and the OpenDyslexic fonts instead.

Hyperlinks use automatic unique destination IDs (`hypertexnames=false`), so the book's intentional visible counter resets do not create colliding PDF targets. Printed equation and chapter numbers are unchanged.
