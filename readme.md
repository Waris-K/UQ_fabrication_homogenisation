# Quantification of Fabrication-Related Uncertainties in TPMS Lattices

This repository contains the summary for **"Quantification of Fabrication-Related Uncertainties in TPMS Lattices with Image Processing and Surrogate Modeling"**, presented at **WCCM 2024 / PANACM 2024**.

## Abstract

This work focuses on quantifying fabrication-induced uncertainties in triply periodic minimal surface (TPMS) lattices using a combination of image processing and surrogate modeling. Geometric deviations were identified using CT scan data and incorporated into finite element (FE) analyses to evaluate the mechanical properties of as-manufactured lattices. A neural network-based surrogate model was developed to predict homogenized Young’s modulus, facilitating efficient uncertainty quantification and optimization.

---

## Methodology

### 1. **Geometric Analysis**
- Conducted micro-CT scans using a SkyScan 1172 microtomograph.
- Applied thresholding and the Otsu method to distinguish solid and void phases.
- Quantified:
  - Equivalent area
  - Eccentricity
  - Centroid shift

### 2. **Finite Element Analysis (FEA)**
- Modeled lattices in **nTop** and analyzed in **ANSYS APDL**.
- Simulated both ideal and as-manufactured geometries with embedded uncertainties.
- Material: **PDMS**, Load: **Compression**, Outputs: **Stress, Strain, and Deformation**.

### 3. **Surrogate Modeling**
- Neural network trained on CT-extracted features (e.g., eccentricity, area, centroid).
- Architecture:
  - Layers: 256-128-64 neurons
  - Optimizer: Adam
  - Metrics: RMSE = 10.536, MAE = 5.184

---

## Key Findings
- Quantified deviations in as-manufactured TPMS lattices using CT scans.
- Performed FEA to evaluate stress-strain responses under compression.
- Developed a neural network surrogate model for predicting homogenized Young's modulus.

---

## Future Work
- Extend methodology to:
  - Non-periodic lattice structures.
  - Functionally graded lattice designs.

---

## Acknowledgements
Supported by:
- **NSF CAREER Award CMMI-2236947**
- **Future Additive Interdisciplinary Manufacturing (FAIM) project** funded by the Office of Naval Research (ONR).

---

## Citation
For citing this work, please use:
