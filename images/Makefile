IMAGES=$(wildcard *.svg)

all: pdf

pdf: $(addsuffix .pdf , $(basename $(IMAGES)))

eps: $(addsuffix .eps , $(basename $(IMAGES)))

%.pdf: %.svg
	inkscape --export-pdf=$@ $<

%.eps: %.svg
	inkscape --export-eps=$@ $<

clean:
	rm *.{pdf,eps}

.PHONY: all pdf eps clean

