# DWARF Constants

This is just a repository that contains all of the constants from [the DWARF
spec](http://dwarfstd.org/doc/DWARF5.pdf) but in a machine readable and program
language agnostic format.

I didn't want to write a LaTeX parser, and it seems like other projects have
all the DWARF constants hard coded in their respective language.  This is a
language agnostic repository of the DWARF constants so that other projects can
write DWARF parsers or generators without copy / pasting from a PDF.

## Frequently Asked Questions

I literally just created this project, so nobody has asked me any questions.

## Questions I Suspect Will Be Asked Frequently

### 1. What is the point of this project?

I wanted to build a DWARF parser in Ruby and it seemed like all DWARF parsers
hard-code the constants in the particular implementation language:

  * https://github.com/gimli-rs/gimli/blob/9630b7442c17e1b3d87ece81bdf17107bfb673e4/src/constants.rs#L93
  * https://github.com/eliben/pyelftools/blob/a347dbfab622ab98d9747d862ade9e6b6fd9425c/elftools/dwarf/constants.py#L12
  * https://github.com/avast/libdwarf/blob/c51918d213fe2daf7ff8b32eb70106fd50f9f4f4/libdwarf/libdwarf/dwarf.h#L57
 
It would be nice if when the DWARF spec is updated that rather than copy /
pasting from a PDF we could just generate the constants.  That's why I made this.

### 2. Why YAML?

I chose YAML over JSON because I could represent numbers in hexadecimal format,
like the spec does.
