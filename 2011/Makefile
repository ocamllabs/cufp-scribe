.PHONY: all clean

%.pdf: %.tex
	pdflatex $*
	pdflatex $*
	pdflatex $*

all: 2011.pdf
	@ :

clean:
	rm -f *.aux *.bbl *.log *.pdf *.ps *.toc
