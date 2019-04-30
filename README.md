This short script will check a _VCF_ files ref bases agaisnt the raw _FASTA_ file, to see if the bases match up. 
It will also check _SAM_ file sequences agaisnt the raw _FASTA_ file and provide a sequence identity percentage.
It will do this based upon the position of the sequences/bases. 

Total stats are produced at the end of the output file.

## PRE-REQUIREMENTS

* [Python 2.7+](https://www.python.org/)
* [PyVCF](https://pyvcf.readthedocs.io/en/latest/)
* [pysam 0.15.2](https://pypi.org/project/pysam/)
* [numpy 1.16.3](https://pypi.org/project/numpy/)
* [argparse 2 0.1.0] (https://pypi.org/project/argparse2/).


## Using the program
Execute ```python seq_check.py -h``` for details of each argument. An example for a _SAM_ and _FASTA_ file use-case would be as executed as follows: 

```python seq_check.py -s ../fruit_fly/fruitfly_77_rna_sortedAligned.out.sam -f     ../fruit_fly/GCA_002310775.1_ASM231077v1_genomic.fa -nosum true -o sam_test```

Where the ```--nosum true``` argument will only produce a summary file

```-v``` would be used instead to specify a VCF file, where ```-s``` specifies a SAM file.
