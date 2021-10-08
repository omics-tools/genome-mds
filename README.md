Genome-MDS
====

<p align="center">
  <img src="https://mitosuite.com/images/for_genome_mds/logo.png" alt="logo" width="200" height="216"/>
</p>

## Description
Genome-MDS: A graphical two-dimensional comparison tool for prokaryotic genomes

## Screenshot

![screenshot](https://mitosuite.com/images/for_genome_mds/genome_mds_preview.gif)

## Installation

1. Install FastANI according the developer's instructions.

・[FastANI](https://github.com/ParBLiSS/FastANI)

2. Install genome-mds with pip

`pip install genome-mds`

## Usage

**Run Genome-MDS**

Please type `genome-mds` on your terminal.

Then, Genome-MDS will open automatically in your browser.

If Genome-MDS does not open, type the localhost address (e.g. http://localhost:8501/) of the streamlit server displayed in your terminal into the address bar of your browser.

## Manual

**STEP0: Go to your working directory**

Go to your working directory. Genome-MDS will run under the working directory.

`cd your_working_directory`

and, then type `genome-mds`.


**STEP1: Set output prefix**

In the first screen, set the name of the output directory. The directories will be created automatically. This directory will contain intermediate files, downloaded arrays, etc. You can also load past runs by putting in the name of the directory you have run before.

<p align="center">
  <img src="https://mitosuite.com/images/for_genome_mds/step1.png" alt="step1"/>
</p>

**STEP2: Upload your genomes**

You should upload your (multiple) genome sequences. The format of the file should be FASTA; a single FASTA should contain only one organism's genome.It is OK to include contigs and plasmids in FASTA, but do not include genomes derived from more than one organism. Files can also be uploaded by drag and drop.　

<p align="center">
  <img src="https://mitosuite.com/images/for_genome_mds/step2.png" alt="step2"/>
</p>

**STEP3: Download sequences**

This step is optional. If you don't need to download anything, select None.
You can automatically download the genomes you want to compare. This corresponds to the Taxonomy ID of NCBI; please enter your email address and the desired Taxonomy ID to query NCBI.Genome-MDS will contact NCBI to get the list of genome sequences first, and you can choose any sequence you want from this list. The selected sequences will be automatically downloaded to the output directory by clicking the Download button.

<p align="center">
  <img src="https://mitosuite.com/images/for_genome_mds/step3.png" alt="step3"/>
</p>

**STEP4: Distance calculation**

In this step, the distances between the genomes are calculated. Here, you can optionally specify the k-mer of ANI calculation and the thread during the calculation. The maximum number of threads for the calculation will be changed according to your PC environment.

<p align="center">
  <img src="https://mitosuite.com/images/for_genome_mds/step4.png" alt="step4"/>
</p>

**STEP5: Interactive MDS**

When the distance calculation is finished, the MDS will be drawn automatically. This MDS can be operated interactively. You can also save the figure.

<p align="center">
  <img src="https://mitosuite.com/images/for_genome_mds/step5_1.png" alt="step5_1"/>
</p>

Interactive MDS allows you to select sequences automatically. This operation allows you to select only the genomes you are interested in. The selected sequences can be downloaded from the automatically generated links.

<p align="center">
  <img src="https://mitosuite.com/images/for_genome_mds/step5_2.png" alt="step5_2" />
</p>

**Exit Genome-MDS**

To exit Genome-MDS, type Control-C in your terminal.

**Optional Run**

Example: change the maximum limit size of file uploadling to 1GB (1024MB).

`genome-mds -M 1024`


## Version

0.0.1

## Licence

[MIT] https://github.com/omics-tools/genome-mds/blob/master/LICENSE
