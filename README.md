# Deduplicator
This script will scan a folder to create a list of input fasta files. It will then use each file in the list it created
and create a two-column format for each sequence.  Paste puts two lines into a single line with space between them. Awk sets up a loop through lines and prints if the expression is true...if the next line is not the same in column 2, it fails to print the line.  Awk results are piped to awk again and it will print column 1, newline, column 2 to recreate the fasta format.  Then it will output the text to a new deduplicated file.

use: bash Deduplicator.sh

Written August 18, 2022 by S. Dean Rider Jr. based on the following:

https://stackoverflow.com/questions/8442459/put-every-alternate-row-in-a-column-using-some-unix-commands <br>
https://www.baeldung.com/linux/uniq-by-column
