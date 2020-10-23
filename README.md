# WeasyPrint-socialscience
Collection of templates for WeasyPrint Typesetting engine, created for social science and humanities

# WORK IN PROGRESS

Homage to the LaTeX Memoir class and inspired by the templates provided by [kjhealy](https://github.com/kjhealy/pandoc-templates). More style might follow.


- Tex Gyre Pagella as base font
- Source Han Serif for CJK (fallback font)
- Source Code Pro as monofont
- Source Sans Pro as sans font (but not used)
- Includes edited chicago-author-year.csl file, optimized for comparative newspaper citations

Credits go to [craigbass76](https://github.com/craigbass76/pandoc-css-weasyprint-template/) who made a repo with useful samples that helped me to understand WeasyPrint's styling syntax.

# How to use

To compile a markdown file to HTML run:

```bash
pandoc 
    -s 
    --template="memoir.html" 
    -f markdown+smart 
    --toc 
    --toc-depth=2 
    -c memoir.css 
    --metadata-file=metadata.yaml 
    --citeproc 
    --csl="csl/chicago-author-date-edited.csl"
    --bibliography=bibiolgraphy.bib 
    input.md 
    -o output.html
```

To compile the html file with [WeasyPrint](https://github.com/Kozea/WeasyPrint):

```bash
python -m weasyprint "output.html" "output.pdf"
```

# Still not pretty

- Table of contents still needs dots leading to the page number
- Title page could be nicer and feature more information
- Footnotes do not work ([problem of WeasyPrint](https://github.com/Kozea/WeasyPrint/issues/298))
- Metadata missing (HTML and PDF)
- Some space could be tighter


# Credits

- Font: [TeX Gyre](https://www.ctan.org/tex-archive/fonts/tex-gyre) used under License: GUST Font License (an instance of the LaTeX Project Public License)

