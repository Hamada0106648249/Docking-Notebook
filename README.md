# Vibe-Coded Docking in Google Colab (AutoDock Vina)  
Install-free molecular docking notebooks for teaching medicinal chemistry, computational chemistry, and pharmacy students.

## Overview
This repository provides two Google Colab notebooks that enable molecular docking directly in a web browser—without requiring local installation of docking software. The notebooks were developed using a **vibe-coding** methodology (prompt-driven code generation with iterative debugging in ChatGPT), combined with **human verification** and reproducibility-oriented checkpoints.

The primary educational objective is to broaden access to professional-style computational experiments for learners with limited coding experience, while maintaining scientific transparency through parameter control and output validation.

## What’s Included
### Notebooks
1. **Notebook 1 — Single-Ligand Docking (SMILES → 3D → Docking)**
   - Dock a single ligand (SMILES input) into a single receptor (PDB input)
   - pH-aware ligand and receptor preparation (Open Babel)
   - Automated docking box estimation from a co-crystallized ligand (when present)
   - Student-adjustable docking parameters (grid center/size, exhaustiveness, poses, verbosity, seed)

2. **Notebook 2 — Library Docking (SMILES list → batch docking)**
   - Dock a **library** of compounds (SMILES file) into a single receptor
   - Parallel ligand preparation + Vina batch docking
   - Export ranked screening results (CSV) + ZIP archive of pose files

### Recommended educational demo target
- **Human ABL1 kinase** crystal structure **PDB ID: 3QRK** (ligand-bound; useful for teaching binding-site definition).
  - RCSB structure page: https://www.rcsb.org/structure/3QRK
  **Human DNA quadrplex** crystal structure **PDB ID: 2MS6**

## How to determine the co-ordinates of the grid box (the binding site)?
After opening the pdb file of the target in PyMOL software, you first select the co-crystallized ligand by left clicking it, 
then in the command line box inside PyMOL type the following command: centerofmass sel. The coordinates in x, y, and z will be typed in the commands screen.
The used grid box size was 20 A in all coordinates

## Quick Start (Open in Colab)
Google Colab is a hosted Jupyter Notebook service that runs Python in the browser and requires no local setup.  

- Notebook 1: [https://research.google.com/colaboratory/faq.html](https://colab.research.google.com/drive/1b9VI6F2KvFQqBiOB-K9LzVWONBPhlpM8?usp=sharing)
- Botebook 2: https://colab.research.google.com/drive/182t3vELC7Gkt-2ke79ASKkCUBbNivlP9

