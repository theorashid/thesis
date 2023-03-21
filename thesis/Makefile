all: pdf html

pdf:
	quarto render --to quarto-thesis-pdf

html:
	find ./Chapters ./Appendices -type f -name '*.qmd' -exec sed -i '' -e "s/.pdf/.webp/" {} \;
	quarto render --to html  --output-dir tmp
	find ./Chapters ./Appendices -type f -name '*.qmd' -exec sed -i '' -e "s/.webp/.pdf/" {} \;
	cp -r tmp/* _thesis/
	rm -rf tmp

docx:
	quarto render --to docx
