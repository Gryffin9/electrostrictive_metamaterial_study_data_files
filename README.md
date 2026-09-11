# Electrostrictive Metamaterial Study Data Files

Simulation and validation data supporting **“Electrostrictive Metamaterial Study: Shaping Fields to Exceed Intrinsic Material Limits.”**

The manuscript and supplementary material are available as a preprint on Zenodo: [doi:10.5281/zenodo.18450271](https://doi.org/10.5281/zenodo.18450271). Journal acceptance or publication is not asserted here.

This repository is a public scientific data companion. It is useful as evidence of simulation post-processing, reproducible data organization, and research-supporting workflows.

## Repository contents

- `02_Slab_Baseline/`: reference slab geometry results.
- `03_Design1_Architected/`: optimized architected design data.
- `04_Design2_Architected/`: alternate optimized architected design data.
- `05_Optimization_Results/`: Nelder-Mead optimization convergence data.
- `06_Validation_Data/`: validation curves and benchmark comparison data.
- `07_Preliminary_Analysis/`: early analysis and stress evolution outputs.
- `README.txt`: detailed file-level documentation and units.

## Data types

The repository includes:

- voltage sweep data,
- displacement, strain, polarization, and stress summaries,
- peak-drive spatial field exports,
- stress distribution images and nodal stress values,
- optimization convergence traces,
- validation curves for polarization and strain response.

## Software context

The data was organized from COMSOL Multiphysics simulation outputs. See `README.txt` for detailed units, folder-level descriptions, and contact information associated with the manuscript.

## Portfolio note

For portfolio readers, this repo demonstrates scientific-computing adjacent work: structuring simulation outputs, documenting units and derived quantities, and preparing supporting data so another researcher can inspect the result without relying on private context.
