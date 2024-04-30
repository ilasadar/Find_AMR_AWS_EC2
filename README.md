# AMR_AWS
Find AMR in AWS - EC2

This script was developed for a Bioinformatics consultation project. If you use it, please cite this GitHub page.

The script is written in Bash. Save the script as 'AMR' (there's no need to add a '.sh' extension).

**Usage:**

```bash
AMR /path/to/paired_end_files {organism}
```

or "if you want to run it in the background"

```bash
nohup AMR /path/to/paired_end_files {organism} > output.out 2> error.out &
```

Paired-end files should be in the format ‘_1.fastq.gz’ and '_2.fastq.gz’.

If you want to download SRR files, use the ‘Download_SRR’ script.

Usage:
```bash
Download_SRR /path/to/text_file
```
The files will be downloaded into the same directory where the text file is located.
