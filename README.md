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

## Domain Boundaries
Functional domain boundaries were based on the following peer-reviewed source:

> Wang, et al. "p53: from understanding its structure to advances in therapeutic targeting." *Signal Transduction and Targeted Therapy* (2026).
> Link: https://www.nature.com/articles/s41392-025-02549-5

The five domains used were:
- Transactivation domain (TAD): 1-61
- Proline-rich domain (PRD): 62-94
- DNA-binding domain (DBD): 95-292
- Tetramerization domain (TD): 325-356
- C-terminal regulatory domain (CTD): 357-393

## Methods
1. Fetched TP53 protein sequences from NCBI using Biopython's Entrez module
2. Performed pairwise alignment of each species against the Human reference sequence
3. Calculated per-position conservation scores across all species
4. Broke down conservation by known functional domain
5. Independently validated results using NCBI BLAST (species-by-species comparison)

## Key Results
- Overall average conservation across species: 58.7%
- Highly conserved positions (≥90% identity): 105 out of 396
- DNA-binding domain (DBD) showed the highest conservation (74.1%), followed by the tetramerization domain (65.6%)
- BLAST comparison of the DBD region (Human vs. each species) confirmed a clear evolutionary gradient:
  - Mouse: 88.72% identity
  - Chicken: 72.83% identity
  - Zebrafish: 71.69% identity
  - Frog: 68.21% identity

## Files
- Analysis notebook (.ipynb)
- Conservation plot along the protein
- Conservation by functional domain (CSV)
- BLAST identity bar chart

## Tools Used
Python, Biopython (Entrez, SeqIO, Align), pandas, matplotlib, NCBI BLAST

## Author
Fatima Shahid — MSc Cancer Biology and Pharmacology, Istinye University
