# AMR_AWS
Find AMR in AWS - EC2

This script was developed for a Bioinformatics consultation project. If you use it, please cite this GitHub page (https://github.com/ilasadar/Find_AMR_AWS_EC2).

The script is written in Bash. Save the script as 'AMR' (there's no need to add a '.sh' extension).

Step 1: Setup conda environment
```bash
conda create -n AMR
conda activate AMR
```
Install dependencies
```bash
conda install bioconda::spades
conda install bioconda::ncbi-amrfinderplus
conda install -c conda-forge -c bioconda -c defaults prokka
```
Install Database for AMRFinder+
```bash
amrfinder -u
```

Install CARD RGI-MAIN and the CARD Database from here, just follow the instructions: 
https://github.com/arpcard/rgi


----------------------------------------

**Usage:**

```bash
AMR /path/to/paired_end_files {organism}
```

or "If you want to run it in the background"

```bash
nohup AMR /path/to/paired_end_files {organism} > output.out 2> error.out &
```

Paired-end files should be in the format ‘_1.fastq.gz’ and '_2.fastq.gz’.

----------------------------------------

If you want to download SRR files, use the ‘Download_SRR’ script.

**Usage:**
```bash
Download_SRR /path/to/text_file
```
The files will be downloaded into the same directory where the text file is located.

----------------------------------------
