TARGETS = EXTRA.pdf c1.pdf c2.pdf c3.pdf c4.pdf c5.pdf c6.pdf c7.pdf c8.pdf c9.pdf c10.pdf c11.pdf c12.pdf

all: $(TARGETS)

%.pdf: %.tex macros.tex
	latexmk $<

clean: 
	rm -f *.aux *.toc *.log *.out *.nav *.snm *.vrb *.blg *.bbl *.synctex.gz *.fdb_latexmk *.fls

distclean: clean
	rm -f $(TARGETS)

.PHONY: all clean distclean
