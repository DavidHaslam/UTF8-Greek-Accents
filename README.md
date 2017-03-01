# UTF8-Greek-Accents
A mapping table to filter [Greek diacritics](https://en.wikipedia.org/wiki/Greek_diacritics) from UTF-8 encoded Unicode text

The main file is a simple tab delimited text file containing two fields:

1. The first field contains the **Find** characters in [PCRE](https://en.wikipedia.org/wiki/Perl_Compatible_Regular_Expressions) format.
2. The second field contains the **Replace** characters as [UTF-8](https://en.wikipedia.org/wiki/UTF-8) byte codes.

The file can be used as an *external replace list* (e.g.) in conjunction with a [TextPipe](http://www.datamystic.com/textpipe/standard.html) filter to implement the following: 

#### Remove Greek Accents from UTF-8 NFC text file

It also replaces GREEK ANO TELEIA by MIDDLE DOT.

- This does not change the [Unicode normalization](https://en.wikipedia.org/wiki/Unicode_equivalence) form from **NFC**.
- It does not remove any Quotation Marks.
- It does not remove any General Diacritics from **NFD** text.

Although principally designed to strip the Greek diacritics from NFC text, it should still work for NFD text.

The mapping table currently has 233 characters, some of which are never seen in Biblical Greek text.
