# sequencing_oneliners
Some sequencing based UNIX one-liners

##count the number of reads in a fastq.gz file
zcat sample.fastq.gz | echo $((`wc -l`/4))
