# Rules for compiling the PDF from the LaTeX sources and displaying the output

### Documents to build
TEX = $(wildcard *.tex)
PDF = $(TEX:.tex=.pdf)
BIB = $(wildcard *.bib)
FIG = $(wildcard figures/*)

all: $(PDF)

show: $(PDF)
	xdg-open $<

%.pdf: %.tex $(BIB) $(FIG)
	tectonic -X compile $<

clean:
	rm -f $(PDF)
