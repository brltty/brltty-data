all: maintenance.html

maintenance.htnml: *.rst

%.html: %.rst
	rst2html $< $@

clean:
	rm -f -- *.html

