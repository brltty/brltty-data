all: maintenance.html

maintenance.html: *.rst

%.html: %.rst
	rst2html $< $@

clean:
	rm -f -- *.html

