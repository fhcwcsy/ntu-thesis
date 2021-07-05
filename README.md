臺灣大學碩博士論文 XeLaTeX 模版
==========

This repo is forked from [the template by Tz-Huan Huang](https://github.com/tzhuan/ntu-thesis).
All credits go to him. Some minor adjustments are:

- Moved to `Biblatex` from `Bibtex` to support more options.
- Used IEEE citation format and support doi hyperlinks on journal issues.
- Add `bachelor` option to document for bachelor degree theses.
- Removed all personal information with dummy texts.
- Isolate font settings to the file `font.tex` since it is rather complex.
- Temporarily removed the watermark feature since it cause unknown compile
errors (tested on TeXLive 2021 on Ubuntu 21.04).

## About fonts

You will need to set the font by yourself in `font.tex`, to work with your
system setup and personal preferences. For normal text font, there's nothing
to worry about. Just look for supported fonts on your computer and add
to `\setCJKmainfont` for Chinese font and `\setmainfont` for English font,
and the same method works for other font families too.

However, the situation becomes tricky if you depend heavily on math (and if
care a lot about beautiful equations like me :D). It doesn't seem to be
clear whether it is required that math font uses Times New Roman (or other
Times-like fonts), but if you want to make math font match with text font,
you will need to change the math font, most likely with an additional package.
What works for me the best is `mtpro2` with `bm` (for bold symbols), but the 
installation of `mtpro2` is a but complicated. As an alternative, you may 
also use `unicode-math`
with `\setmathfont{TeX Gyre Termes Math}`, if you don't care about the ugly
integral symbol. You may find many other solutions on 
[google](https://www.google.com/search?q=LaTeX+math+font+times) too. 

As for `mtpro2`, you can download the lite version (which is sufficient for most
people) [here](https://www.ctan.org/pkg/mtp2lite) (the link on the 
[official site](https://www.pctex.com/mtpro2.html)  seems to be broken), and
follow the instructions [here](https://pctex.com/kb/62.html) (you may also
try [this](https://github.com/jamespfennell/mathtime-installer) but it
didn't work for me). I have uploaded an `mtpro2` (lite) archive in the repo
too. You may need 
[this](https://askubuntu.com/questions/66498/setting-tex-live-path-for-root) 
if writing on your TexLive directories requires root privilege.

For some basics about fonts families (Serif, Sans, mono, etc), see, for example,
[here](https://www.w3schools.com/css/css_font.asp). 

