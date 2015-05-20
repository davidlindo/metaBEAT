# metaBEAT
Metabarcoding analyses pipeline

```bash

usage: metaBEAT.py [options] REFlist

optional arguments:
  -h, --help            show this help message and exit
  -Q <FILE>, --querylist <FILE>
                        file containing a list of query files
  -v, --verbose         turn verbose output on
  -s, --seqinfo         write out seq_info.csv file
  -f, --fasta           write out ref.fasta file
  -p, --phyloplace      perform phylogenetic placement
  -t, --taxids          write out taxid.txt file
  -b, --blast           compile local blast db and blast queries
  -m <string>, --marker <string>
                        marker ID (default: marker)
  -n <INT>, --n_threads <INT>
                        Number of threads (default: 1)
  -E, --extract_centroid_reads
                        extract centroid reads to files
  -e, --extract_all_reads
                        extract reads to files
  --version             show program's version number and exit

Query:
  The parameters in this group affect how the query sequences are processed

  --trim_adapter <FILE>
                        trim adapters provided in file
  --trim_qual <INT>     minimum phred quality score (default: 30)
  --trim_window <INT>   sliding window size (default: 5) for trimming; if average quality drops below the specified minimum quality all subsequent bases are removed from the reads
  --trim_minlength <INT>
                        minimum length of reads to be retained after trimming (default: 50)
  --merge               attempt to merge paired-end reads
  --product_length <INT>
                        estimated length of PCR product (default: 100)
  --phred <INT>         phred quality score offset - 33 or 64 (default: 33)

Reference:
  The parameters in this group affect the reference to be used in the analyses

  -R <FILE>, --REFlist <FILE>
                        file containing a list of files to be used as reference sequences
  --gb_out <FILE>       output the corrected gb file
  --rec_check           check records to be used as reference

Clustering options:
  The parameters in this group affect read clustering

  --clust_match <FLOAT>
                        identity threshold for clustering in percent (default: 1)
  --clust_cov <INT>     minimum number of records in cluster (default: 1)

BLAST search:
  The parameters in this group affect BLAST search and BLAST based taxonomic assignment

  --www                 perform online BLAST search against nt database
  --min_ident <FLOAT>   minimum identity threshold in percent (default: 0.95)
  --min_bit <INT>       minimum bitscore (default: 80)

```
