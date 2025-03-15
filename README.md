# UTF8-Greek-Accents
A mapping table to filter [Greek diacritics](https://en.wikipedia.org/wiki/Greek_diacritics) from UTF-8 encoded Unicode text

The main file is a simple tab delimited text file containing two fields:

1. The first field contains the **Find** characters in [PCRE](https://en.wikipedia.org/wiki/Perl_Compatible_Regular_Expressions) format.
2. The second field contains the **Replace** characters as [UTF-8](https://en.wikipedia.org/wiki/UTF-8) byte codes.

The file can be used as an *external replace list* (e.g.) in conjunction with a [TextPipe](http://www.datamystic.com/textpipe/standard.html) filter to implement the following: 

#### Remove Greek Accents from UTF-8 NFC text file

It also replaces GREEK ANO TELEIA by MIDDLE DOT.

- This does not change the [Unicode normalization](https://en.wikipedia.org/wiki/Unicode_equivalence) form from **NFC**.
- It does not remove any **Quotation Marks**.
- It does not remove any General Diacritics from **NFD** text.

Although principally designed to strip the Greek diacritics from NFC text, it should still work for NFD text.

The mapping table currently has 233 characters, some of which are never seen in [Biblical Greek](https://en.wikipedia.org/wiki/Koine_Greek) text.

The simple mapping table was prepared using Excel. My workbook has also been uploaded for transparency.

Each worksheet is protected but without a password merely to prevent inadvertent changes. Autofilter is permitted.

The derived copy of the mapping table in which the file name ends with **BC** uses Byte Codes in the Find column.

**Acknowledgement**: The excellent Unicode text editor for Windows called [BabelPad](http://www.babelstone.co.uk/Software/BabelPad.html) was invaluable in preparing this file.

My bespoke TextPipe filter has now been uploaded.

Most users will need to edit the absolute path for the external replace list file.

Currently, this is "C:\Users\David\TextPipe Filters\Custom\Greek\UTF8GreekAccents.tab"

*And not every Windows user is called David.*
