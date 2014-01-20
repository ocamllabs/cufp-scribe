paper = cufp13
figs = 

.PHONY: clean pdf

$(paper).pdf: $(figs) $(paper).tex $(paper).bib
	pdflatex $(paper) ;\
	bibtex $(paper) ;\
	pdflatex $(paper) ;\
	pdflatex $(paper)

%.pdf: %.dot
	dot -Tpdf $< > $@

$(paper).ps: $(paper).dvi
	dvips $(paper)

pdf: $(paper).pdf

clean:
	rm -f $(paper).ps $(paper).pdf \
	  $(paper).log $(paper).bbl \
	  $(paper).blg $(paper).aux \
	  $(paper).toc \
	  $(figs)

$(paper).tar.gz : $(figs) $(paper).tex $(paper).bib
	tar -czvf $(paper).tar.gz $^

tarball: $(paper).tar.gz
