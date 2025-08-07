FILE = notes
TEX_FILES := $(FILE).tex macros.tex n1.tex n2.tex n3.tex n4.tex n5.tex n6.tex n7.tex n8.tex n9.tex n10.tex n11.tex n12.tex n13.tex shortcut.tex n20.tex n21.tex n22.tex n23.tex n24.tex n25.tex n26.tex n27.tex n28.tex

all: $(FILE).pdf

%.pdf: %.tex $(TEX_FILES)
	pdflatex -synctex=1 $<
	pdflatex -synctex=1 $<

clean: 
	rm -f *.aux *.toc *.log *.out *.nav *.snm *.vrb *.blg *.bbl *.synctex.gz

distclean: clean
	rm -f *.pdf 

.PHONY: handout handouts all clean distclean
