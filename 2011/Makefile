.PHONY: all clean

%.pdf: %.tex biblio.bib
	pdflatex $*
	bibtex $*
	pdflatex $*
	pdflatex $*


all: 2011.pdf
	@ :

clean:
	rm -f *.aux *.bbl *.log *.pdf *.ps *.toc
