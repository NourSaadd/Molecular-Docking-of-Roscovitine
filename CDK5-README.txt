# CDK5 Docking Files

This directory contains all input and output files related to the molecular docking of **Roscovitine** with **Cyclin-Dependent Kinase 5 (CDK5)**.

## Contents

- `cdk5_clean.pdb`  
  Cleaned PDB file of CDK5.

- `cdk5.pdbqt`  
  Receptor file generated from `cdk5_clean.pdb`. Includes hydrogens and Gasteiger charges.

- `roscovitine.pdb`  
  Original **Roscovitine ligand structure**.

- `roscovitine.pdbqt`  
  Ligand file derived from `roscovitine.pdb`. Prepared by adding hydrogens, computing charges, and defining torsions.

- `cdk5.gpf`  
  Grid parameter file defining the docking box around the binding site.

- `cdk5.dpf`  
  Docking parameter file for AutoDock4 using the Lamarckian Genetic Algorithm.

- `cdk5.glg`  
  Grid log file from AutoGrid4.

- `cdk5.dlg`  
  Docking log file containing docking runs and energies.

- `cluster_summary.txt` *(if present)*  
  Clustering results based on RMSD threshold.

- `visualization/` *(optional)*  
  Chimera session for receptor-ligand interaction and superposition with CDK2.

## Notes

- Ligand preparation was consistent with CDK2
- Docking used the same LGA parameters
- Best binding energy: -7.68 kcal/mol
- CDK5 exhibited more flexible binding poses
- Both entropy values (CDK2 and CDK5) were 0.45, indicating stable clustering
