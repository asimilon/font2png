# font2png
A little Python tool to convert a TrueType (ttf/otf) font into a PNG for use in demos.

To use from command line it expects `python3` to be at `/usr/bin`, it also expects that [Pillow](https://github.com/python-pillow/Pillow) is installed and available to Python.

```
font2png -f <font file> -o <output file> -w <width> -l -s <scale) -m -d -h
  --font=<font file>     (-f) - font to use (ttf or otf)
  --output=<output file> (-o) - PNG file to be output
  --width=<num. pixels>  (-w) - width in pixels of output (minimum 8 pixels)
  --left-align           (-l) - left align the font (default centred)
  --scale                (-s) - font scale relative to width (defult 1.0)
  --mono                 (-m) - output as monochrome
  --defines              (-d) - output letter widths to stdout
  --help                 (-h) - show usage
```

After exporting to PNG use your [favourite tool to convert](http://deadliners.net/ImageTool/index.html) to a format suitable for your demo.

The output is one giant tall image where each `<width>` sized box contains a character, in ASCII order, starting with `SPACE` (32) and ending with `~` (126).

I will gladly accept pull requests for any improvements that can be made.