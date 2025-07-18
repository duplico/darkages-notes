.PHONY = all_pdfs clean
.DEFAULT_GOAL = docs_combined.pdf

*.drawio.pdf:
#	for file in $(shell ls *.drawio.svg); do drawio --embed-diagram --export --format pdf $$file; done
	echo $@

all_pdfs:
	for file in $(shell ls *.drawio.svg); do drawio --embed-diagram --export --format pdf $$file; done

docs_combined.pdf: all_pdfs
	pdfunite *.drawio.pdf docs_combined.pdf

clean:
	$(RM) *.drawio.pdf docs_combined.pdf
