---
title: Latex markup language
subtitle: This section is aimed at introducing you to the basics of LaTeX.

# Summary for listings and search engines
summary: Latex uses a special markup language, transforming the source text along with its markup into a high-quality document.
# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
  

tags:
  - Academic
  

categories:
  - Demo

---



## Content

First, the user needs to prepare a file with text equipped
commands for LaTeX, which traditionally has a .tex extension. Further
the procedures take place in two stages:

1. First of all, you should process the file using a translator program. IN
the result will be a file with the extension .dvi (device-independent, that is, independent
from the device).

2. Further, the generated file, also called a dvi-file, can be used using programs
which are called dvi drivers, print on a laser or dot matrix
printer, look at the screen, and so on. If the results are unsatisfactory,
the user can make changes to the source file, after which the cycle repeats.
The source file for the LaTeX system is the actual text of the document along with
special characters and commands with which instructions should be transmitted to the system
regarding text placement. This file can be generated using any
text editor, but in this case it is necessary that the so-called
pure text file (ASCII file). This means that the text should not contain
font highlighting, pagination, and the like.
The source text of the document cannot have hyphens (LaTeX will generate them itself). Words
must be separated by spaces, but LaTeX does not distinguish how many
The user left spaces between words. The end of the line is also treated as
space. Individual paragraphs must be separated from each other by blank lines.
Most of the characters in the source text directly represent what follows
print (if there is a comma in the source text, then there will be a comma in the print). A
The following characters have a special status:

{ } $ & # % _ ~ ~ \ & # % _ ~ ~ \

If one of these characters is used simply in the text, then most likely it will be issued
error message. A printed display of the first seven characters can be obtained if
In the source text, place the “\” sign before the corresponding character without a space.
When the % symbol is used in text other than as part of the \% combination, it is considered
“comment character”, that is, all characters that are located on the line after it,
the program ignores. Using the % symbol, marks can be added to the source text
with the status “for yourself”.
Curly braces delimit groups in the source file. Dollar symbol limits
mathematical formulas. When entering mathematical formulas, the _ and ^ signs are used (“the sign
underscore" and "lid"). The ~ sign is intended to indicate a "non-breaking space" between
words. All LaTeX commands begin with a \. The # and & signs are used in more
complex LaTeX constructions.

![](images.jpg)


