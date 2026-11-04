# drb

Read the Douay-Rheims Bible from your terminal

A separate program from `kjv`, built from the same shell/awk code, but
with the Douay-Rheims text in place of the King James text. The text
is the Douay-Rheims Bible, Challoner revision, in the Catholic canon
of 73 books, with the deuterocanonical books in their usual places
and Douay-Rheims book names and numbering (for example, 1 and 2 Kings
for Samuel, 3 and 4 Kings for Kings, Paralipomena for Chronicles, and
Apocalypse for Revelation).

The verse data (`drb.tsv`) is in the same 6-column format as `kjv.tsv`
and is derived from the Douay-Rheims reading in the
[bbl](https://github.com/thenewmantis/bbl) project, itself a derivative
of the `kjv` terminal Bible program.

## Usage

    usage: ./drb [flags] [reference...]

      -l      list books
      -W      no line wrap
      -h      show help

      Reference types:
          <Book>
              Individual book

          <Book>:<Chapter>
              Individual chapter of a book

          <Book>:<Chapter>:<Verse>[,<Verse>]...
              Individual verse(s) of a specific chapter of a book

          <Book>:<Chapter>-<Chapter>
              Range of chapters in a book

          <Book>:<Chapter>:<Verse>-<Verse>
              Range of verses in a book chapter

          <Book>:<Chapter>:<Verse>-<Chapter>:<Verse>
              Range of chapters and verses in a book

          /<Search>
              All verses that match a pattern

          <Book>/<Search>
              All verses in a book that match a pattern

          <Book>:<Chapter>/<Search>
              All verses in a chapter of a book that match a pattern

## Build

drb can be built by cloning the repository and then running make:

    git clone https://github.com/donaldturnbull/douay-rheims.git
    cd douay-rheims
    sudo make install

## License

Public domain
