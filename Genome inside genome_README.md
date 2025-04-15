## 🔧 What It Does

The pipeline includes the following steps:

1. Download SRA data using `prefetch`
2. Convert `.sra` to FASTQ using `fasterq-dump`
3. Compress FASTQ files with `gzip`
4. Run quality control checks using `FastQC`
5. Trim reads using `Trimmomatic`
6. Assemble reads into contigs with `MEGAHIT`
7. Perform BLASTn search on assembled contigs against a fungal reference database
