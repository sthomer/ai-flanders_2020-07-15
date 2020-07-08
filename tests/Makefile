departments=etro brubotics soft ai
outputname=test.pdf \
		   $(departments:=-beamer.pdf)

BEAMERSTY=../beamerthemevub.sty \
          ../beamercolorthemevub.sty \
          ../beamerfontthemevub.sty \
          ../beamerinnerthemevub.sty \
          ../beamerouterthemevub.sty \
		  ../vubprivate.sty \

.PHONY: clean all

all: $(outputname)

%.pdf: %.tex $(BEAMERSTY)
	export TEXINPUTS="$(PWD)/..":$$TEXINPUTS; \
	latexmk -pdf -xelatex -latexoption='--shell-escape' -use-make $*

%-beamer.tex: beamer-department.tex $(BEAMERSTY)
	cp beamer-department.tex $*-beamer.tex
	sed -ie s/DEPARTMENT/$*/ $*-beamer.tex


clean:
	latexmk -c -C
	rm _minted-main -rf
