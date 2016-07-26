# sequencing_oneliners
Some sequencing based UNIX one-liners

##count the number of reads in a fastq.gz file
``zcat sample.fastq.gz | echo $((\`wc -l\`/4))``

##using fastx_trimmer to trim all your reads to a specific length (discarding those that are below that length) e.g. 51 bases in this example
``http://hannonlab.cshl.edu/fastx_toolkit/index.html``

uses the -Q 33 flag for Phred+33 which is not mentioned in ./fastx_trimmer -h

``fastx_trimmer -Q 33 -v -f 1 -l 51 -i sample.fq -o sample_trimmed.fq``
