CC = gcc

all: task.pdf task.svg task.png

task.svg: task.dot
	dot -Tsvg task.dot > task.svg

task.pdf: task.dot
	dot -Tpdf task.dot > task.pdf

task.png: task.dot
	dot -Tpng task.dot > task.png

href: task.dot gen-href
	egrep -o "[0-9]*" task.dot | sort | uniq | ./gen-href > href

area-naive: area-naive

clean:
	-rm *.svg *.pdf *.png
