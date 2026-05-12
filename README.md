# BST281_Final_Proj
This README encompasses all analyses conducted by Skylar Ann Gay for BST 281 Spring 2026 for Module 1. This README, code files, data, and dependencies are publicly available on GitHub at https://github.com/sagay2022/BST281_Final_Proj/tree/main.

## Dependencies 
### O2 Based Analyses
(Conda) Miniforge3 24.11.3-0 

Python 3.10.20

bcftools 1.23.1

bowtie2 2.5.5

ncbi-datasets-cli 18.23.0

samtools 1.23.1

sra-tools 3.4.1

Prokka 1.15.6

Glimmer 3

### R Bases Analyses
R 4.5.2

Biostrings 2.78.0

dplyr 1.1.4

stringr 1.6.0

purr 1.2.1

tidyr 1.3.2

ggplot2 4.0.2

patchwork 1.3.2

## Code Files
All O2 
### Assembly_O2_Workflow
### Glimmer_O2_Workflow
### R_Prokka_Dataframe_Manipulation
### R_Pangenome_Analysis

## Data Files
### SAG_BActerodies_caccae_assembly_4-20-26.fa


### SAG_hypothetical_aa_calls.csv
### SAG_hypothetical_dna_calls.csv
### SAG_ncbi_merged_aa_calls.csv
### SAG_ncbi_merged_dna_calls.csv

### Annotation (directory)
### Assembly (directory)


### NCBI_pangenome_annotations (directory .tsv files)
This directory contains 13 .tsv files of genome annotations obtained from NCBI with the cooresponding accession number. Each file contains columns for gene Accession, Begin, End, Chromosome, Orientation, Name, Symbol, Gene ID, Gene Type, Transcripts accession, Protein accession, Protein length, and the Locus tag. These files contain protein coding genes, pseudogenes, tRNAs, and rRNAs.

|Species | Reference strain | Accession # |
| -------- | -------- | -------- |
| Bacteroides uniformis | JCM5828 | GCA_044361425.1 |
| Alistipes putredinis | DSM 17216 |GCA_000154465.1 |
| Ruminococcus bromii | min17_bin57 | GCA_928721825.1 |
| Roseburia faecis | JCM 17581 | GCA_045061065.1 |
| Lachnospira eligens | ATCC 27750 | GCA_000146185.1 |
| Fusicatenibacter saccharivorans | AM67-22ACA | GCA_027667425.1 |
| Bifidobacterium adolescentis | ATCC 15703 | GCA_000010425.1 |
| Parabacteroides distasonis | APCS2/PD | GCA_018279895.1 |
| Collinsella aerofaciens | JCM 10188 | GCA_010509075.1 |
| Akkermansia muciniphila | JCM 30893 | GCA_009731575.1 |
| Anaerostipes hadrus | BA1 | GCA_030864025.1 |
| Bacteroides caccae | CL03T12C61 | GCA_018292205.1 |
| Roseburia inulinivorans | FDAARGOS_1587 | GCA_020731525.1 |

### NCBI_pangenome_annotations > protein_coding_NCBI.csv
This .csv is the result of R_Pangenome_Analysis line 23. This contains file compiles the .tsv files in the NCBI_pangenome_annotations directory into a .csv, filtering down to rows containing only the protein-coding genes identified in the annotations. Each file contains columns for gene Accession, Begin, End, Chromosome, Orientation, Name, Symbol, Gene ID, Gene Type, Transcripts accession, Protein accession, Protein length, and Locus tag, and the Source file- including the organism name.

## Data Pulled from External Sources
### Reference genome
|Species | Reference strain | Accession # |
| -------- | -------- | -------- |
| Bacteroides caccae | CL03T12C61 | GCA_018292205.1 |

This is the recognized reference strain for *Bacteroides caccae*. I directly accessed this sequence while working in O2 (Assembly_o2_Workflow; lines 17-19).

### Sequencing reads
I obtained sequencing reads from SRA: ERR13818447. This sequencing was conducted at the Monash Institute of Medical Research and used Illumina NovaSeq 6000 paired-end sequencing with a result of 81.9M bases, published on 2025-06-05. I pulled these directly into O2 using prefetch (Assembly_o2_Workflow; lines 23-24).
