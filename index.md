---
layout: single
title: Nanjing University - Cheminformatics and Modelling (19003220 / 083100D01) - Fall 2026
classes: wide
no_toc: true
show_title: false
header:
  overlay_image: /assets/banner.png
  overlay_filter: 0.15
  caption: "Nanjing University - Cheminformatics and Modelling - Fall 2026"
  alt: "Cheminformatics and Modelling"
---

This is a crash course in the computational tools of structure-based drug design: conformational analysis, protein-ligand docking, molecular dynamics, free energy methods, and electronic structure calculation. In an era where machine learning can predict almost any property you ask it to, understanding requires physics-based tools to validate predictions.

This is not a criticism of AI, but rather a necessity to shape your contribution as a researcher, as well as an understanding of the failure modes of both techniques. Machine learning and atomistic models fail in **different and uncorrelated ways**, and that is exactly what makes them useful together. A machine-learned model fails when a query falls outside its training distribution, and it fails silently — the prediction comes back with the same confidence either way. A force field fails when its parameters do not cover your chemistry. A docking score fails because it discards entropy and solvation. A tight-binding method fails where its approximations are known to break down. Those failures are things you can anticipate, and they are not the same failures the ML model is making.

So when a model hands you a ranked list of a thousand compounds, you do not have to choose between believing it and ignoring it. You can take the top of the list, put it through a method whose assumptions you understand, and see whether the ranking survives. Where the two agree, you have something worth spending money on. Where they disagree, you have learned something about at least one of them. Every method in this course is cheap compared to synthesis and assay, and that is the point: **the purpose of these tools is to tell you what is worth committing real resources to.**

Each week asks the same two questions of a new method: **what does it actually compute, and what did it throw away in order to be fast enough to run?**

## Levels of Theory

| Method | What it discards | What it buys you |
|---|---|---|
| Conformer generation | Everything but sterics and torsional strain | The geometry every other method assumes |
| Docking | Entropy, solvation, protein flexibility | Enrichment — not binding affinity |
| Molecular dynamics | Electrons; bond making and breaking | Dynamics, flexibility, explicit solvent |
| Free energy methods | Still no electrons | An actual ΔG, at real computational cost |
| Tight binding / DFT | Scale | Reactivity, covalent chemistry, metals |

---

# Turn in Your Homework
- [Upload Here](https://box.nju.edu.cn/u/d/c976fcfdddb84109a2b1/)
- **Format**: Student Number - Name - HW# .pdf / .ipynb
- **Example**: 12345678-Prof.Chris-HW1.pdf

---
## Course Schedule

### Class 1 - (Sep 18): Levels of Theory and the Minimum Toolkit
Molecular representations, RDKit, and chemical file formats — SMILES, SDF, PDB, protonation states, and what a "structure" actually is. Framing for the semester.

- **Slides**: [View Slides]()
- **Homework**: [Assignment 1 - Working with Chemical Descriptors](https://www.kaggle.com/code/chrisbutch/nju-cheminformatics-and-modelling-class-1)
- **Required Reading**: Krenn et al. (Aspuru-Guzik group) [On Scientific Understanding with Artificial Intelligence] 
  [Nature.com link](https://www.nature.com/articles/s42254-022-00518-3)   
  [NJU Download](https://box.nju.edu.cn/f/4c4d5196ff014c36af15/)  

- **Suggested Reading**: Messeri and Crockett [Artificial intelligence and illusions of understanding in scientific research] 
  [Nature.com link](https://www.nature.com/articles/s41586-024-07146-0)   
  [NJU Download](https://box.nju.edu.cn/f/71f763a7a08046338a00/)  

### Class 2 - (Oct 9): Conformers and Force Fields
Where molecular geometry comes from. Conformer generation, torsional sampling, force field functional forms, and how many conformers is enough.

### Class 3 - (Oct 16): Docking I — Scoring Functions
What a docking score is made of, term by term, and why it is not a binding affinity.

### Class 4 - (Oct 23): Docking II — Screening at Scale and Predicted Structures
Enrichment, library preparation, pose validation, and fragment-based approaches. Docking into predicted structures, and why a static prediction may not give you the right rotamer.

### Class 5 - (Oct 30): Molecular Dynamics I — Fundamentals
Integrators, thermostats, periodic boundaries, and explicit solvation. What flexibility costs.

### Class 6 - (Nov 13): Molecular Dynamics II — Running and Analyzing a System
Trajectory analysis, convergence, and what you can and cannot conclude from a simulation of a given length.

### Class 7 - (Nov 20): Free Energy Methods
MM/GBSA through FEP. The bridge from enrichment to ΔG, and what it costs to cross it.

### Class 8 - (Nov 27): Electronic Structure, Tight Binding, and ML Potentials
GFN2-xTB and semi-empirical methods. When you need electrons, how to get them affordably, and where machine-learned potentials are converging with force fields.

### Class 9 - (Dec 4): Reactivity and Covalent Inhibitors
Where classical methods structurally cannot go — bond making and breaking, warhead reactivity, reaction path scouting.

### Class 10 - (Dec 11): **Exam**
In class.

### Class 11 - (Dec 18): Project Work
Supervised development time.

### Class 12 - (Dec 25): **Project Presentations**

---

## Additional Resources:
- [Course Syllabus](https://box.nju.edu.cn/f/f136a0eaa23d45a79c10/)
- [Project Guidelines](https://box.nju.edu.cn/f/141c396eb52a4a19b10e/)
- [FAQ]({{ '/faq/' | relative_url }})
