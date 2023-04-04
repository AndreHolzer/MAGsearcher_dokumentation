<a href='https://github.com/AndreHolzer/MAGsearcher'><img src='images/MAGsearcher-hex.png' align="right" height="180" /></a>

# Usage

[{% octicon arrow-left height:32 class:"right left" vertical-align:middle aria-label:hi %}](GS_T.md) [{% octicon home height:32 class:"right left" aria-label:hi %}](index.md) [{% octicon arrow-right height:32 class:"right left" aria-label:hi %}](US_E.md)

----



## Required input data and format

The tool handles two different inputs, the GC/MS peak list data (metabolite vs. peak intensity), as well as an optional file containing sample information including dry weights.

> **ATTENTION**: FILE NAMES MUST NOT CONTAIN ANY SPACES



MAGsearcher facilitates the search of a set of user defined queries against MAG or single-genome derived proteomes and/or other uses defined proteins sequences. As the algorithm operates on amino acid level, either protein files (in fasta format: .fasta, .faa or .fa) can be used or metagenome based nucleotide assemblies (in fasta format: .fna) alongside an annotation file (in .gff format) must be provided. 

Metagenomic data should be in an uncompressed form and organised in a folder structure representing independent samples. In case no protein fasta files are present, initial pre-processing of the metagenomic information is performed in order to generate a list of protein templates. Pre-processing steps include conversion of the .gff files into an R readable format, the import gff and 

 

Next, we import the combined.gff file into R and add MAG bin information to .gff file and .faa information to the .gff file. We write this out to a file at: '../common_data/faa_mag_bins.csv' and additionally, we write a .faa file for every one of the 1338 MAG bins, which we will use later. We subsequently create .faa files for MAGs that have the same species-level annotation; this is useful later on when we want to assess MAGs from hotsprings assigned to the same species, but we don’t want to exclude all low completeness MAGs. 

 

We run ‘./15_download_refseq_genus.sh’ to download any additional genera of interest. 





### 1. GCMS data (required)
GCMS data must contain information on Compounds, Response time (RT) and Peak Intensity (Response) and can be provided in several formats. Several files of the same format can be processed and merged together during a single Metapolish analysis run.

- `.pdf`: format from Thermo analysis output is supported and once loaded will be converted into .tsv format ([see example input](https://github.com/AndreHolzer/Metapolish/blob/master/example_data/input/Thermo-Xcaliber-Tracefinder/Thermo-example_output_1.pdf))


- `.tsv`: format containing three columns (Compound, Retention time, Response) ([see example input](https://github.com/AndreHolzer/Metapolish/blob/master/example_data/input/Sample1.tsv))


- `.csv`: format containing three columns (Compound, Retention time, Response) ([see example input](https://github.com/AndreHolzer/Metapolish/blob/master/example_data/input/Sample1.tsv))


- `.xlsx`: format with first sheet containing three columns (Compound, Retention time, Response) or in Shimadzu output format ([see example input](https://github.com/AndreHolzer/Metapolish/blob/master/example_data/input/Shimadzu_GCMSsolution/1_1_fame.xlsx))

   
### 2. Dry weights (optional)
Dry weight information for the individual samples can be provided in a tab separate file of the following format:

   | Sample                            | DW          | Unit                 |
   | --------------------------------- | ----------- | -------------------- |
   | \<File name including extension\> | \<integer\> | \<character string\> |
   | \<File name including extension\> | \<integer\> | \<character string\> |
   | \<File name including extension\> | \<integer\> | \<character string\> |

   > **IMPORTANT**: DO NOT USE ANY OTHER COLUMN NAMES

For convineince you can simply adjust the [Sample_info.tsv](example_data/Sample_info.tsv) example file to macth your samples.




----
Let's have a look at jow to [execute the anylsis](US_E.md)
