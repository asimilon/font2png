# font2png

A little Python tool to convert a TrueType (ttf/otf) font into a PNG for use in demos.

To use from command line it expects `python3` to be at `/usr/bin`, it also expects that [Pillow](https://github.com/python-pillow/Pillow) is installed and available to Python.

```
font2png -f <font file> -o <output file> -s <size> -w <width> -y <height> -l -m -d -i <index> -h
  --font=<font file>        (-f) - font to use (ttf or otf)
  --output=<output file>    (-o) - PNG file to be output
  --size=<num. pixels>      (-s) - font size
  --width=<num. pixels>     (-w) - width in pixels of output (defaults to font size rounded up to multiple of 8)
  --height=<num. pixels>    (-y) - height in pixels of output (defaults to font size)
  --left-align              (-l) - left align the font (default centred)
  --mono                    (-m) - output as monochrome
  --defines                 (-d) - output letter widths to stdout
  --quantise=<num. colours> (-q) - quantise colours to number specified
  --index=<face index>      (-i) - which font face to load (default first available face)
  --help                    (-h) - show usage

```

After exporting to PNG use your [favourite tool to convert](http://deadliners.net/ImageTool/index.html) to a format suitable for your demo.

The output is one giant tall image where each `<width>` sized box contains a character, in ASCII order, starting with `SPACE` (32) and ending with `~` (126).

I will gladly accept pull requests for any improvements that can be made.
