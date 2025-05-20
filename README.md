# Vertical Ground Motion Effects on URM Structures (Vertical-GM-URM)

This repository contains the data and numerical models used in the study:

Kallioras S, Graziotti F, Magenes G. Vertical accelerations in seismic analysis: A numerical investigation of their effects on URM structures. *Earthquake Spectra* 2025. DOI: pending.

## Overview

This study investigates the influence of vertical ground motions on unreinforced masonry (URM) structures through nonlinear time-history analyses (NLTHA) using equivalent frame (EF) models. Vertical seismic effects are often overlooked in the seismic assessment of masonry buildings. This work highlights their significance and provides a reproducible numerical dataset to support further research.

The materials in this repository enable researchers and engineers to:
- Understand how vertical ground motion affects the seismic response of URM buildings;
- Extend or adapt the EF models for new scenarios or parametric studies;
- Reproduce key figures, results, and performance indicators discussed in the paper.

## Repository Structure

- `TremuriModels/` – EF models developed using the academic version of the analysis software *TREMURI*.
- `GroundMotions/` – Input three-component ground motions for the cloud analysis.
- `Dataset/` – Processed output data in `.mat` format (e.g., displacements, drift ratios).

## Getting Started

To explore the models and data:

```bash
git clone https://github.com/SteliosKallioras/Vertical-GM-URM.git
