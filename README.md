# ECS Network Analysis

This repository contains the datasets, results, and reproducible workflows for our systems-level study of the **endocannabinoid system (ECS)**.  
We integrate protein–protein and protein–chemical interactions into unified network models to uncover the organizational principles and resilience of ECS signaling.





## Google Colab Notebook
You can explore the full analysis pipeline in Google Colab here:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1iCT5JWlePddg06106nOp34V0XjywODFk?usp=sharing)

*The notebook is view-only. To run or modify, please use **File → Save a copy in Drive**.*





## Network Construction (Summary)
- **Proteins**: Forty ECS-associated proteins curated from literature, UniProt, and STRING. Metadata includes amino acid sequences, localization, complexes, and structures (via SIFTS + PDB). Protein–protein interactions were obtained from STRING (confidence ≥ 0.7).  
- **Chemicals**: Forty ECS-relevant chemicals (endocannabinoids AEA & 2-AG, phytocannabinoids THC & CBD, selected eicosanoids) curated from literature, PubChem, and ChEMBL. Metadata includes IUPAC names, SMILES strings, and RDKit-derived descriptors. Protein–chemical interactions were filtered to include only ECS proteins.  
- **Networks**: Three networks were constructed in NetworkX:  
  - Protein–protein only  
  - Protein–chemical only  
  - Combined (all interactions)  
- **Analyses**:  
  - Centrality (betweenness, closeness, degree, eigenvector) to quantify influence.  
  - Louvain clustering to identify functional modules.  
  - Perturbation analysis to assess robustness after targeted hub removal.  





## Repository Structure
ecs_data/
├── data/
│ ├── Edges/ # PPI & PCI edge lists
│ └── Nodes/ # Protein & chemical node metadata
├── results/
│ ├── Combined Network/ # Centrality, clustering, perturbations, visualizations
│ ├── P-P-Only Network/ # Protein–protein analyses
│ └── P-C-Only Network/ # Protein–chemical analyses
├── manuscript/ # Placeholder (PDF will be added here)
└── folder_structure.txt # Full directory tree





## Example Visualization
*Combined protein–chemical ECS network*  

![Combined ECS Network](ecs_data/results/Combined%20Network/Network%20Visualization/ecs_combined_network.png)





## Dependencies
All dependencies are pre-installed in the provided Colab notebook.  
For standalone runs, install:

pip install requests
pip install numpy==1.24.4
pip install rdkit-pypi
pip install python-louvain





Collaborators
Aanya Shridhar (A.S.) — Data curation, network construction, computational analyses, visualizations; analyzed and interpreted results; co-wrote the manuscript.

Sugyan Mani Dixit (S.M.D.) — Conceived and supervised the project, designed the framework, co-analyzed results, and co-wrote the manuscript.

Reggie Gaudino (R.G.) — Provided insights on results, contributed manuscript edits, and supported the research through funding.





Citation
If you use this repository, please cite the corresponding paper once published.

BibTeX:
[INSERT BIBTEX]
