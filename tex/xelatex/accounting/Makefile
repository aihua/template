TEX = latex
XETEX = xelatex
DVI2PDF = dvipdfmx
MAKEINDEX = makeindex
GBK2UNI = gbk2uni

OBJECTS = main

all:	$(OBJECTS)

$(OBJECTS) : clean
	$(XETEX) $@
	$(XETEX) $@
	rm -fr *.aux *.dvi *.log *.out *.out.bak *.toc *.thm *.idx *.ind *.ilg
	
book: clean
	$(XETEX) $@
	$(XETEX) $@
	$(MAKEINDEX) $@
	$(XETEX) $@
	rm -fr *.aux *.dvi *.log *.out *.out.bak *.toc *.thm *.idx *.ind *.ilg

clean:
	rm -fr *.aux *.dvi *.log *.out *.out.bak *.toc *.pdf *.thm *.idx *.ind *.ilg
	cd chapter ; rm -fr *.aux *.dvi *.log *.out *.out.bak *.toc *.pdf *.thm *.idx *.ind *.ilg
