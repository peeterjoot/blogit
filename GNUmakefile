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
