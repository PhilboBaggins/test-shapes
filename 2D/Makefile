SRC_FILES := $(wildcard *.scad)
DXF_FILES := $(patsubst %.scad,%.dxf,$(SRC_FILES))
SVG_FILES := $(patsubst %.scad,%.svg,$(SRC_FILES))

.PHONY: all clean

all: $(DXF_FILES) $(SVG_FILES)

%.dxf: %.scad
	openscad -o $@ $<

%.svg: %.scad
	openscad -o $@ $<

clean:
	rm -f $(DXF_FILES)
	rm -f $(SVG_FILES)
