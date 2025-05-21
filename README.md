# Vertical-GM-URM: Vertical Ground Motion Effects on URM Structures

This repository contains the data and numerical models used in the study:

**Kallioras S., Graziotti F., Magenes G.**  
*Vertical accelerations in seismic analysis: A numerical investigation of their effects on URM structures.*  
*Earthquake Spectra*, 2025. DOI: pending.

---

## Overview

This paper investigates the potential influence of vertical ground motions on a case-study unreinforced masonry (URM) building through nonlinear time-history analyses (NLTHA) using equivalent frame (EF) models. Vertical components are often neglected in seismic assessments of masonry buildings. This work examines their role in selected structural response parameters under a range of modelling assumptions and ground motion scenarios.

The dataset and models provided here allow full reproduction of the numerical results and figures presented in the publication. Specifically, this repository enables researchers and engineers to:
- Examine how vertical ground motion may affect the seismic response of URM buildings;
- Extend or modify the EF models for additional parametric studies;
- Reproduce key outputs and response indicators presented in the paper.

---

## Repository Structure

- `TremuriModels/` – EF models developed using the academic version of the *TREMURI* software. Includes the mother file and all model variations used in the analyses. A `Model_Variations.md` file provides a detailed description of each parametric set.

- `GroundMotions/` – Contains 249 `.acc` files corresponding to 83 ground motions, each with three components (EW, NS, UD).  
  - Format: single-column ASCII (.acc)  
  - Units: **m/s²**  
  - Time step: **0.005 s**

- `Dataset/` – Contains 8 `.mat` files, each corresponding to one of the analysis sets presented in Table 2 of the paper: *A-1*, *A-2*, *B-1*, *B-2*, *C-1*, *C-2*, *C-3*, and *C-4*. Set names are aligned with those described in the [`Model_Variations.md`](TremuriModels/Model_Variations.md) file. For more details on the dataset format and contents, see [`Dataset_Description.md`](Dataset/Dataset_Description.md).

    Each `.mat` file includes:
    
    - **Two data matrices** (each with 83 rows and 4 columns) containing maximum displacement demands: one for **slender pier walls** (i.e., "*Windows*" wall) and one for **squat pier walls** (i.e., "*Doors*" wall). Units are in **mm**. NaN values indicate collapse, as defined in the paper. Matrix columns are organised as follows:
        1. Demand under H1 only  
        2. Demand under H2 only  
        3. Demand under combined H1 + V  
        4. Demand under combined H2 + V  

    - **A matrix of ground motion record IDs** (83 rows × 4 columns), listing the applied records for each analysis case, ordered consistently with the data matrix rows.

---

## Citation

If you use this dataset or the associated models, please cite the following paper:

Kallioras S., Graziotti F., Magenes G. Vertical accelerations in seismic analysis: A numerical investigation of their effects on URM structures. *Earthquake Spectra* 2025. DOI: *pending*.

Please do **not** cite the dataset directly. The dataset was created to support the findings presented in the above publication.

---

## License

This dataset is licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to use, share, and adapt the material for any purpose, including commercial, as long as you cite the paper above and credit the authors: Stylianos Kallioras, Francesco Graziotti, Guido Magenes.

---

## Getting Started

You can clone the repository or download it as a ZIP archive.  
Open the EF models in *TREMURI* to inspect input configurations and modelling assumptions.  
Load the `.mat` files in MATLAB (or compatible software) to analyse and visualise displacement demands.

To clone via Git:

```bash
git clone https://github.com/SteliosKallioras/Vertical-GM-URM.git
