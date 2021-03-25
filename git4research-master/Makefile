html:
	Rscript -e 'bookdown::render_book("index.Rmd", output_format = "bookdown::gitbook", clean = FALSE)'
	cp -fvr style.css _book/
	# cp -fvr images _book/
	# cp -fvr _main.utf8.md _book/main.md

build:
	make html
	Rscript -e 'browseURL("_book/index.html")'

cleaner:
	make clean && rm -fvr rsconnect
	rm -frv *.aux *.out  *.toc # Latex output
	rm -fvr *.html # rogue html files
	rm -fvr *utf8.md # rogue md files

