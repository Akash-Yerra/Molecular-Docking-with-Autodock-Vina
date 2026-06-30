![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-research-orange)
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

## 🧬 Protein Targets Included

This repository presents molecular docking studies on six experimentally resolved protein structures obtained from the **RCSB Protein Data Bank (PDB)**. These proteins were selected because they represent important therapeutic targets in antiviral, anticancer, and anti-inflammatory drug discovery. For each protein, both **Active Site Docking** and **Blind Docking** experiments were performed using **AutoDock Vina**.

### 📌 Protein Summary

| **PDB ID** | **Protein** | **Disease Area** | **Co-crystallized Ligand** | **Repository Contents** |
|:---------:|-------------|------------------|----------------------------|-------------------------|
| **1HSG** | HIV-1 Protease | HIV/AIDS | Protease Inhibitor | Active Site Docking, Blind Docking |
| **1HVR** | HIV-1 Protease | HIV/AIDS | Cyclic Urea Inhibitor | Active Site Docking, Blind Docking |
| **1IEP** | c-Abl Tyrosine Kinase | Chronic Myeloid Leukemia (CML) | Imatinib (Gleevec) | Active Site Docking, Blind Docking |
| **1OCE** | Cyclooxygenase (COX) Enzyme | Inflammation & Pain | Anti-inflammatory Ligand | Active Site Docking, Blind Docking |
| **6XQS** | SARS-CoV-2 Main Protease (Mpro / 3CLpro) | COVID-19 | Telaprevir | Active Site Docking, Blind Docking |
| **8CYZ** | SARS-CoV-2 Main Protease (Mpro / 3CLpro) | COVID-19 | Compound C4 | Active Site Docking, Blind Docking |

**Note:** The native (co-crystallized) ligands available in the PDB structures were used for docking studies of **1HSG**, **1HVR**, **1IEP**, and **1OCE** to reproduce and analyze experimentally observed binding interactions. For the SARS-CoV-2 Main Protease structures (**6XQS** and **8CYZ**), **Carmofur** was used as the docking ligand because it is a well-known inhibitor of the viral main protease and has been widely investigated in COVID-19 antiviral drug discovery.
---

## 📖 Protein Descriptions

### 🦠 HIV Drug Discovery

#### **1HSG – HIV-1 Protease**
HIV-1 Protease is an essential viral enzyme responsible for cleaving viral polyproteins into functional proteins required for viral maturation. Inhibiting this enzyme prevents the production of infectious HIV particles, making it one of the primary targets for anti-HIV drug development.

#### **1HVR – HIV-1 Protease**
This structure also represents HIV-1 Protease but is crystallized with a different inhibitor. It is widely used in molecular docking studies for evaluating protease inhibitors and understanding protein–ligand interactions involved in HIV therapy.

---

### 🎗️ Cancer Drug Discovery

#### **1IEP – c-Abl Tyrosine Kinase**
The c-Abl Tyrosine Kinase regulates cell growth, differentiation, and survival. Abnormal activation of this kinase is associated with Chronic Myeloid Leukemia (CML). This structure contains the well-known anticancer drug **Imatinib (Gleevec)** and is considered a landmark example of structure-based drug design.

---

### 💊 Anti-inflammatory Drug Discovery

#### **1OCE – Cyclooxygenase (COX)**
Cyclooxygenase (COX) is a key enzyme involved in prostaglandin biosynthesis, which mediates inflammation, pain, and fever. It is one of the most important therapeutic targets for Non-Steroidal Anti-Inflammatory Drugs (NSAIDs), making it a common protein for molecular docking and virtual screening studies.

---

### 🦠 COVID-19 Antiviral Drug Discovery

#### **6XQS – SARS-CoV-2 Main Protease (Mpro / 3CLpro)**
This structure represents the SARS-CoV-2 Main Protease in complex with **Telaprevir**, an antiviral drug originally developed against Hepatitis C Virus (HCV). Since the Main Protease is essential for viral replication and absent in humans, it is considered one of the most promising therapeutic targets for COVID-19 drug discovery.

#### **8CYZ – SARS-CoV-2 Main Protease (Mpro / 3CLpro)**
This structure contains the SARS-CoV-2 Main Protease bound to **Compound C4**, an experimental inhibitor. It provides valuable structural information for understanding inhibitor binding mechanisms and supports the rational design of next-generation antiviral compounds against COVID-19.

Each protein contains:

- Active Site Docking
- Blind Docking


---

# Software Used

- AutoDock Vina
- AutoDock Tools (ADT)
- PyRx(for blind docking)
- Open Babel(with in the PyRx)
- PyMOL (for visualization)
- Protein Data Bank (PDB)
- PubChem (DataBase)

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
https://bioinformaticsreview.com/20161214/how-to-perform-docking-in-a-specific-binding-site-using-autodock-vina/

2. Protein Data Bank

https://www.rcsb.org/

3. PubChem

https://pubchem.ncbi.nlm.nih.gov/

---

# Repository Highlights

1. Multiple proteins

2. Active Site Docking

3. Blind Docking

4. Complete docking workflow

5. Ready-to-use AutoDock Vina files

6. Beginner-friendly organization

7. Suitable for students, researchers, and bioinformatics learners

---

# Author

**Yerra Akash**

B.Tech Computer Science and Engineering

Research Interest:
- Quantum Computing
- Drug Discovery
- Molecular Docking
- Quantum Machine Learning

