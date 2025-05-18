# Molecular Docking of Roscovitine with CDK2 and CDK5

This project investigates the molecular docking of **Roscovitine**, a cyclin-dependent kinase (CDK) inhibitor, with **CDK2** and **CDK5**, which are key regulators of the cell cycle and potential drug targets for cancer and neurodegenerative diseases.

The study involves:
- Structural preparation of CDK2 and CDK5
- Ligand cleaning and flexibility setup
- Grid box parameterization
- Docking simulations using AutoDock4 with the Lamarckian Genetic Algorithm (LGA)
- Binding energy analysis, conformational clustering, and visualization

This repository contains:
- All docking files for **CDK2** and **CDK5**, including `.pdbqt`, `.gpf`, `.dpf`, and `.dlg` files
- A complete scientific **report** in DOCX format detailing methodology, results, and structural analysis

## Objectives

- Compare the binding conformations and interaction energies of Roscovitine with CDK2 and CDK5
- Evaluate selectivity and structural compatibility
- Visualize docking results and assess alignment with experimental structures

## Receptor and Ligand Preparation

- **CDK2 (PDB ID: 2A4L)**: Cleaned by removing water molecules, hydrogen atoms added, and Gasteiger charges computed. Chain A retained.
- **CDK5**: Extracted chain A from the full structure, cleaned similarly to CDK2.
- **Ligand (Roscovitine)**: Extracted from CDK2 crystal structure, water removed, torsion tree root identified, and charges computed. Found to have 8 rotatable bonds.

## Docking Protocol

- **Software**: AutoDockTools 1.5.7, AutoDock4, Chimera, PyMOL
- **Docking Algorithm**: Lamarckian Genetic Algorithm (LGA)
- **Grid Dimensions**: 60 × 60 × 60 with spacing 0.375 Å
- **Parameters**:
  - 100 docking runs
  - Population size: 150
  - Max evaluations: 2,500,000
  - Mutation rate: 0.02
  - Crossover rate: 0.8

## Results

### CDK2

- Best binding energy: **-7.76 kcal/mol** (Run 99)
- Clustering: 18 clusters with RMSD ≤ 2.0 Å
- Most populated cluster: Cluster 1 (37 members)
- Key interactions:
  - **Hydrogen bonds**: LYS33, LEU83
  - **Pi-cation interaction**: Observed
  - **Hydrophobic interaction**: VAL18
- RMSD with crystal structure: **1.205 Å**
- Entropy: 0.45

### CDK5

- Best binding energy: **-7.68 kcal/mol**
- Similar entropy (0.45), indicating consistent clustering
- Slightly more variable binding poses
- Greater angular diversity (quaternion comparison)
- Unique binding interactions not seen in CDK2

### Structural Comparison

- CDK2 and CDK5 show high sequence identity (~47%)
- Structures superposed using Chimera show highly conserved folds and aligned ligand binding pockets
- Chain break observed in CDK2 but not in CDK5
- Ligands align well between both structures with minor positional shifts

## Tools and Formats

- `.pdb` / `.pdbqt`: Receptor and ligand files
- `.gpf`, `.dpf`, `.glg`, `.dlg`: AutoGrid and AutoDock parameter and result files
- `.docx`: Full scientific report
- Chimera: Used for visualization and structural alignment

## Team

This project was completed as part of an academic computational biology course by:

- Nour Saad 
- Lynn Oueidat 
