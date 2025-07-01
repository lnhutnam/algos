# Compiler and flags
PDFLATEX = pdflatex
PDFLATEX_FLAGS = --interaction=nonstopmode
CLEAN_FILES = *.aux *.log *.out *.toc *.bbl *.blg *.idx *.ilg *.ind *.nav *.snm *.vrb *.dvi

# Default target
all: template_slides.pdf

# Build the PDF
template_slides.pdf: template_slides.tex
	$(PDFLATEX) $(PDFLATEX_FLAGS) $<
	$(PDFLATEX) $(PDFLATEX_FLAGS) $<  # Run twice for references and TOC

# Clean auxiliary files
clean:
	rm -f $(CLEAN_FILES)

# Clean all including PDF
distclean: clean
	rm -f template_slides.pdf

.PHONY: all clean distclean