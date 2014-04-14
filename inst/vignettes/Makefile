LATEXFILES = *.aux\
        *.bbl\
        *.blg\
        *.ilg\
        *.log\
        *.nlo\
        *.nls\
        *.toc\
        *.aux\
	Rplots.pdf\
	*.dvi\
	*.map\
        *.out\
	isingLenzMC.tex\
        *pdf\
        *dvi\
        *ps\
        *Rout\

all:
	make clean
	make vignette

setvars:
ifeq (${R_HOME},)
R_HOME= $(shell R RHOME)
endif

vignette:
	"$(R_HOME)/bin/R" CMD BATCH run.R

clean:
	rm -f $(LATEXFILES)
	rm -f *~
	rm -f .Rhistory
	rm -f isingLenzMC.R
	rm -f isingLenzMC.tex

cacheclean:
	make clean
	rm -fr vigsrc/cache vigsrc/figure 
	rm -f vigsrc/F063721.dat-mztab.txt
	rm -f vigsrc/TMT_Erwinia_1uLSike_Top10HCD_isol2_45stepped_60min_01.mzXML
	rm -f vigsrc/P00924.fasta

