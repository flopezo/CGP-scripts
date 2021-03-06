# CGP-scripts

Scripts for the Caenorhabditis genome project

### kmer_histo.R
Creates an R histogram plot from the kmc_tools histogram output
```
kmer_histo.R histo.txt
```
### clc_insert.pl
Outputs the insert size of the reads from clc mapping
```
clc_insert.pl \
-c [lib.cas] \   # The cas file
-i \             # Output the insert sizes
-o [lib] \       # Output prefix
-lib [lib]       # Lib name
```
### sam_insert.pl
Outputs the insert size of the reads from bowtie mapping 
```
sam_insert.pl \
-s [lib.sam] \    # The sam file
-f [contigs.fa] \ # The assembly file
-i \              # Output the insert sizes
-o [lib] \        # Output prefix
-l [lib]          # Lib name
```
### plot_insert_freq_txt_binned.R
Creates an R histogram plot from clc_insert.pl output
```
Requires ggplot2

plot_insert_freq_txt_binned.R [lib.cas.insert.freq.txt]
```
### daa_to_tagc.pl
Creates a tagc readable format from dianmond's daa. Download uniref100.taxlist from [here](https://github.com/GDKO/uniref_taxlist)
```
Requires diamond in the path

daa_to_tagc.pl uniref100.taxlist [assembly_se_uniref.daa]
```
### keep_unmapped_reads.pl
Retains unmapped paired end reads from a sam file
```
keep_unmapped_reads.pl [Lib.sam] >[clean_1.fq] 2>[clean_2.fq]
```
### keep_unmapped_reads_se.pl
Retains unmapped single end reads from a sam file
```
keep_unmapped_reads_se.pl [Lib.sam] >[clean_1.fq]
```
### groc_sam.pl
Extracts paired reads that do not map to a contig list from sam
```
groc_sam.pl [list] [Lib.sam]
```
### groc_sam_se.pl
Extracts single end reads that do not map to a contig list from sam (i.e for merged reads)
```
groc_sam_se.pl [list] [Lib.sam]
```
### assembly.rename.sh
Renames the scaffolds of the assembly
```
Requires fastaqual_select.pl in path

assembly.rename.sh [assembly] [scaffold_name] # eg nCe.2.0
```
### fastaqual_select.pl
Executes different operations in a fasta file
```
To get a list of operations run

fastaqual_select.pl 
```
