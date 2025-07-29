# 🧬 Golden Gate Plasmid Checker

A Python GUI tool to validate plasmid sequencing results from a Golden Gate assembly. This tool checks `.ab1` sequencing files for quality, extracts inserted gRNA sequences, and compares them to a reference list from a primer CSV. It also matches the gRNAs against the corresponding `.fasta` files and summarizes all results in a clean CSV report.

---

## ✨ Features

- GUI interface using PySimpleGUI
- Loads a list of expected gRNAs from a CSV (with uppercase letters only)
- Processes a folder containing `.ab1` and `.fasta` files
- Checks average sequencing quality (Phred scores)
- Extracts inserted gRNA from sequencing reads
- Searches for matching gRNAs within `.fasta` plasmid sequences
- Outputs a summary `.csv` file with quality metrics and match results

---

## 📁 Input File Format

### Primer CSV

The CSV should use `;` as delimiter and contain at least the following two columns:

```csv
name;sequence
sgRNA_1;tttGAGTCCGAGCAGAAGAAGaaac
sgRNA_2;tttTTTGCCTACGAGGTTGTCGaaac
...

## Installation
conda create -n biopython python=3.10
conda activate biopython
pip install biopython pandas PySimpleGUI
