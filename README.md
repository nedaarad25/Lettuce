# 🧬 Fungal Sequence Processing Pipeline

This repository contains a bash script to automate the processing of SRA sequencing data. It performs a complete workflow from downloading raw data to generating assembled contigs and performing a BLASTn search against a fungal database.

---

## 🔧 What It Does

The pipeline includes the following steps:

1. Download SRA data using `prefetch`
2. Convert `.sra` to FASTQ using `fasterq-dump`
3. Compress FASTQ files with `gzip`
4. Run quality control checks using `FastQC`
5. Trim reads using `Trimmomatic`
6. Assemble reads into contigs with `MEGAHIT`
7. Perform BLASTn search on assembled contigs against a fungal reference database

---

## 🚀 Usage

Edit the script variables at the top of `pipeline.sh`:

```bash
SRA_ID="SRRXXXXXXX"
PROJECT_NAME="YourProject"
BASE_DIR="/your/path/to/output"
TMP_DIR="/your/path/to/temp"
THREADS=16
FASTQ_THREADS=12
ADAPTER_FILE="TruSeq3-PE.fa"
BLAST_DB="fungi_database"
