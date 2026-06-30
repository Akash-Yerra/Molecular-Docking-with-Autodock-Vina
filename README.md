# Molecular Docking using AutoDock Vina

> A complete hands-on molecular docking project demonstrating both **Active Site Docking** and **Blind Docking** using **AutoDock Vina** on multiple protein targets.

---

# Overview

This repository contains molecular docking experiments performed using **AutoDock Vina**.

The objective of this project is to demonstrate the complete workflow of molecular docking, starting from raw protein structures downloaded from the Protein Data Bank (PDB) to obtaining docking poses and analyzing binding affinities.

The repository has been organized in a way that beginners can understand every stage of the docking process while also serving as a reference for researchers.

---

# Project Objectives

This project demonstrates:

- Protein preparation
- Ligand preparation
- Active Site Docking
- Blind Docking
- AutoDock Vina configuration
- Analysis of docking results
- Comparison of docking strategies

---

# Repository Structure

```
Molecular Docking/
│
├── MOLECULAR DOCKING WITH AUTODOCK VINA.pdf
│
├── 1HSG/
│   ├── Active site docking/
│   └── Blind docking/
│
├── 1HVR/
│   ├── active site docking/
│   └── blind docking/
│
├── 1IEP/
│   ├── Active site docking/
│   └── Blind docking/
│
├── 1OCE/
│   ├── Active site docking/
│   └── Blind docking/
│
├── 6XQS/
│   ├── Activesite Docking/
│   └── BlindDocking/
│
└── 8CYZ/
    ├── Active site docking/
    └── blind docking/
```

Each protein folder represents a complete docking experiment.

---

# Protein Targets Included

| Protein ID | Description |
|------------|-------------|
| 1HSG | Protein docking example |
| 1HVR | Protein docking example |
| 1IEP | Protein docking example |
| 1OCE | Protein docking example |
| 6XQS | Protein docking example |
| 8CYZ | Protein docking example |

Each protein contains:

- Active Site Docking
- Blind Docking

allowing comparison between both approaches.

---

# Software Used

- AutoDock Vina
- AutoDock Tools (ADT)
- Open Babel
- PyMOL (for visualization)
- Protein Data Bank (PDB)
- PubChem

---

# Molecular Docking Workflow

The complete workflow followed in this repository is shown below.

```
Protein Selection
        │
        ▼
Download Protein (.pdb)
        │
        ▼
Protein Cleaning
(Remove Water, Ligands)
        │
        ▼
Protein Preparation (.pdbqt)
        │
        ▼
Ligand Preparation
        │
        ▼
Create Configuration File
        │
        ▼
Run AutoDock Vina
        │
        ▼
Obtain Docking Poses
        │
        ▼
Analyze Binding Affinity
        │
        ▼
Visualize in PyMOL
```

---

# Active Site Docking

Active Site Docking is performed when the binding pocket of the protein is already known.

The search space is restricted only to the active site.

Advantages

- Faster
- More accurate
- Lower computational cost
- Suitable when binding pocket is known

Each Active Site Docking folder contains:

- Protein (.pdb)
- Clean protein
- Protein (.pdbqt)
- Ligand
- Ligand (.pdbqt)
- Configuration file
- Docking output

---

# Blind Docking

Blind Docking is performed when the binding pocket is unknown.

Instead of searching only one pocket, AutoDock Vina searches the entire protein surface.

Advantages

- Useful for unknown proteins
- Can identify novel binding pockets

Disadvantages

- Slower
- Larger search space

---

# Folder Explanation

## Protein File (.pdb)

Original protein downloaded from the Protein Data Bank.

Example

```
1HSG.pdb
```

---

## Clean Protein

Protein after removing

- Water molecules
- Co-crystallized ligands
- Unwanted atoms

Example

```
1HSG_clean.pdb
```

---

## Protein PDBQT

Prepared protein required by AutoDock Vina.

Contains

- Atom types
- Charges
- Hydrogens

Example

```
1HSG_clean.pdbqt
```

---

## Ligand

Ligand molecule used for docking.

Examples

```
ligand.mol2
ligand.pdb
```

---

## Ligand PDBQT

Prepared ligand for AutoDock Vina.

Example

```
ligand.pdbqt
```

---

## Configuration File

Example

```
conf.txt
```

This file defines the docking search box.

Typical parameters include

- center_x
- center_y
- center_z
- size_x
- size_y
- size_z
- exhaustiveness

---

## Docking Output

Example

```
vina_output.pdbqt
```

This file contains

- Best binding pose
- Alternative poses
- Binding affinity
- Atomic coordinates

---

# How to Run

## Step 1

Prepare receptor

```
prepare_receptor4.py
```

---

## Step 2

Prepare ligand

```
prepare_ligand4.py
```

---

## Step 3

Run AutoDock Vina

```
vina --receptor protein.pdbqt \
     --ligand ligand.pdbqt \
     --config conf.txt \
     --out output.pdbqt
```

---

# Understanding the Results

AutoDock Vina reports

```
Mode
Binding Affinity
RMSD
```

Example

```
Mode  Affinity (kcal/mol)

1     -9.2
2     -8.7
3     -8.5
```

Generally,

- More negative affinity indicates stronger predicted binding.
- The first mode usually represents the best predicted binding pose.

---

# Visualization

The docking poses can be visualized using

- PyMOL
- AutoDock Tools
- Discovery Studio Visualizer

Load

- Protein
- Docked ligand

to inspect molecular interactions.

---

# Learning Outcomes

After exploring this repository, readers will understand

- Protein preparation
- Ligand preparation
- PDB and PDBQT formats
- Active Site Docking
- Blind Docking
- Configuration files
- AutoDock Vina workflow
- Binding affinity interpretation
- Docking output analysis

---

# References

1. AutoDock Vina Documentation

https://autodock-vina.readthedocs.io/

2. Protein Data Bank

https://www.rcsb.org/

3. PubChem

https://pubchem.ncbi.nlm.nih.gov/

---

# Repository Highlights

✔ Multiple proteins

✔ Active Site Docking

✔ Blind Docking

✔ Complete docking workflow

✔ Ready-to-use AutoDock Vina files

✔ Beginner-friendly organization

✔ Suitable for students, researchers, and bioinformatics learners

---

# Author

**Yerra Akash**

B.Tech Computer Science and Engineering

Research Interest:
- Quantum Computing
- Drug Discovery
- Molecular Docking
- Quantum Machine Learning

GitHub:
https://github.com/Akash-Yerra
