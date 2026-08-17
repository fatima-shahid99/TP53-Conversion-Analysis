# TP53 Conservation Analysis Across Species

## Research Question
Which regions of the TP53 tumor suppressor protein are most conserved across species?

## Overview
This project compares TP53 protein sequences from five vertebrate species (Human, Mouse, Chicken, Zebrafish, and Frog) to identify which regions of the protein have remained evolutionarily conserved, and whether this pattern aligns with known functional domains.

## Data Source
Protein sequences were retrieved from NCBI RefSeq:
- Human: NP_001394193.1
- Mouse: NP_035770.2
- Chicken: NP_990595.1
- Zebrafish: NP_001258749.1
- Frog: NP_001001903.1

## Methods
1. Fetched TP53 protein sequences from NCBI using Biopython's Entrez module
2. Performed pairwise alignment of each species against the Human reference sequence
3. Calculated per-position conservation scores across all species
4. Broke down conservation by known functional domain
5. Independently validated results using NCBI BLAST

## Key Results
- Overall average conservation across species: 58.7%
- Highly conserved positions (≥90% identity): 105 out of 396
- DNA-binding domain (DBD) showed the highest conservation (70.3%) compared to other functional regions
- BLAST comparison of the DBD region confirmed high sequence identity (87.36%, E-value = 3e-60)

## Files
- `TP53_Conversion_Analysis_Final.ipynb` — full analysis notebook
- `tp53_conservation_plot.png` — conservation plot along the protein
- `tp53_conservation_by_domain.csv` — conservation scores by functional domain

## Tools Used
Python, Biopython (Entrez, SeqIO, Align), pandas, matplotlib, NCBI BLAST

## Author
Fatima Shahid — MSc Cancer Biology and Pharmacology, Istinye University
