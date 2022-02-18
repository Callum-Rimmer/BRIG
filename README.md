# BRIG
## Setting up BRIG
1. Download the latest version of BRIG from the offical website: https://sourceforge.net/projects/brig/

2. There is no installation process for BRIG, it is run from a `BRIG.jar` file. Therefore unzip the BRIG folder in the desired location.

## Installing BLAST
You can download the latest version of BLAST from the official NCBI website: https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/

For **Windows** users, download the file ending with `win64.exe`. This is a bundled installer for windows which will install BLAST for you.

For **macOS** users, download the file ending with `.dmg`. You have to do some more legwork to install BLAST on macOS.

## The problem with BRIG

Normally with BRIG you can upload you reference and query sequences and it will genereate the BLAST rings. The query sequences you use however must be one sequence each i.e. one gene or a complete genome (only one contig). If you want to use mutliple genes or a genome in multiple contigs as your query sequence for a BLAST ring BRIG will treat this as a standard multi-fasta file and will not generate the ring properly. Follow the next steps in order to add a multi-fasta file as a ring.

There are two main scenarios for dealing with multi-fasta files:

- Are you using a genome in multiple contigs?
- Are you using a number of genes in one fasta file?

### Running BRIG with a genome in multiple contigs

This is the easiest of the two scenarios. The easiest way of running BRIG with a multiple-contig genome is to simply remove all header lines in the fasta file after the inital header line. Use the following command to do this:

```head -n 1 | grep -v ">" genome.fasta > genome-without-headers.fasta```

