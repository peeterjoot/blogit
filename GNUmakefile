THISDIR := curvilinear
THISBOOK := $(THISDIR)

include ../latex/make.vars

FIGURES := ../figures/$(THISBOOK)
SOURCE_DIRS += $(FIGURES)

GENERATED_PDFS += cramersga.pdf
GENERATED_PDFS += multivector.pdf
GENERATED_PDFS += hyperwedge.pdf

all :: $(COPIED_FILES)
$(GENERATED_PDFS) :: Bibliography.bib myrefs.bib
all :: $(GENERATED_PDFS)
#all :: d4x.pdf
#all :: xtox.pdf

#$(THISBOOK).pdf :: $(wildcard *.tex)
#$(GENERATED_PDFS) :: $(JUSTBOOKDEPENDENCIES) $(LOCAL_FILES) $(GENERATED_SOURCES) $(COPIED_FILES) $(LOCAL_COPIED_FILES) Bibliography.bib
#$(GENERATED_PDFS) :: $(JUSTBOOKDEPENDENCIES) $(LOCAL_FILES) $(GENERATED_SOURCES) $(COPIED_FILES) $(LOCAL_COPIED_FILES) Bibliography.bib

include ../latex/make.rules

%.sp : %.tex
	spellcheck $^
	touch $@

# mv rule doesn't work.  do it manually.
mathstyle.sty :
	wget --output-document=$@ http://tug.org/svn/texlive/trunk/Master/texmf-dist/tex/latex/breqn/mathstyle.sty?revision=54801&view=co

multivector.pdf :: vectorasarrow.tex
multivector.pdf :: inthepipe.tex
multivector.pdf :: vectorspace.tex
