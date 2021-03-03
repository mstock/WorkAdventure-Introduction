SVGFILES := $(wildcard *.svg)
MINSVGS := $(SVGFILES:%.svg=%.png)

all: $(MINSVGS)

%.png : %.svg
	perl -ni -e 'unless (m{sodipodi\:absref}) { print $$_ }' $<
	rsvg-convert $< > $@

clean:
	rm -v *.png
