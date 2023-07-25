slides-for-meetecho.pdf: slides.pdf
	# Workaround for meetecho doing slides at fixed DPI rather than fixed
	# size in pixels
	#
	# Thanks Kurt Pfeifle at https://stackoverflow.com/a/7507511
	gs \
	 -o $@ \
	 -sDEVICE=pdfwrite \
	 -g16000x9000 \
	 -dFIXEDMEDIA \
	 -dPDFFitPage \
	 -dCompatibilityLevel=1.4 \
	  $<

slides.pdf: slides.tex slides-99-core-consolidated-slides-06.pdf
	lualatex $<

slides-99-core-consolidated-slides-06.pdf:
	curl https://www.ietf.org/proceedings/99/slides/$@ > $@
