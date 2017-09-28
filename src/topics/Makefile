TEX = pdflatex
# $dst is destination worksheet where to put in pdf

%:
	cd $(*) && \
	$(TEX) -output-directory=../../logs *.tex && \
	cd ../../logs && \
	rm -r *.aux *.log *.out && \
	if [ -d ../pdf/$(dst) ]; then echo "file exists"; else mkdir ../pdf/$(dst); fi && \
	mv worksheet$(*).pdf ../pdf/worksheet$(*)/ && \