# Note! This project was uploaded as a complete file and has been sent to the journal of Astronomy and Astrophysics for peer-review as of March, 2026.

Authors:
Diya A. Lansberg, UC Berkeley
Mariusz Tarnopolski, Institute of Astronomy, Faculty of Physics, Astronomy and Informatics, Nicolaus Copernicus University

# LSBC Filament Distance Analysis  

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)  
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)  
![Status](https://img.shields.io/badge/Status-Research%20Project-success.svg)  
![License](https://img.shields.io/badge/License-MIT-green.svg)  

---

## Overview  

This project reproduces and extends the analysis of the relationship between **X-ray surface brightness (SBX)** and **distance to the nearest cosmic filament (D₍fila₎)** for low surface brightness clusters (LSBCs).

The project:
- Reproduces prior results on SBX–filament distance relationships  
- Computes distances using multiple methods  
- Evaluates statistical significance using Monte Carlo simulations  

---

## Key Concepts  

- **SBX (Surface Brightness)** → traces intracluster gas  
- **D₍fila₎ (Filament Distance)** → measures cluster environment  
- **Cosmic Filaments** → large-scale structure of the universe  

---

## Example Visualization  

[comparison_averages.pdf](https://github.com/user-attachments/files/26338049/comparison_averages.pdf)

![Example Plot](Outputs/comparison_averages.pdf)

---

## Features  

- KD-Tree nearest neighbor search  
- Haversine (spherical) distance calculations  
- Redshift-sliced analysis (Δz = 0.005)  
- Monte Carlo simulations (~10⁴ runs)  
- Permutation testing for statistical significance  
- Error propagation in logarithmic space  

---

## Project Structure
- Zarattini_replication.ipynb (all code)
- Data
- Outputs
- README.md


---

## Methodology  

### Distance Computation  
- KDTree (fast approximation)  
- Haversine distance (accurate spherical geometry using Astropy)  

Distances are computed within redshift slices to match filament catalogs.

### Surface Brightness  
Derived from X-ray luminosity and cluster mass, analyzed in log-space with uncertainties.

### Classification  
Clusters are grouped into:
- Low surface brightness (LSB)  
- Intermediate surface brightness (ISB)  
- High surface brightness (HSB)  

### Monte Carlo Analysis  
- Random sampling  
- Permutation testing  
- Subsampling  
- Error propagation  

---

## Key Results  

- Correlation between SBX and filament distance is not robust  
- Results depend strongly on the filament catalog used  
- High probability that observed patterns arise from chance  
- Small sample sizes limit statistical significance  

---
## Usage
Clone the repository:
git clone https://github.com/your-username/lsbc-filament-analysis.git

cd lsbc-filament-analysis

Launch Jupyter:
jupyter notebook

Open:
notebooks/Zarattini_replication.ipynb
Run all cells

## Installation  

```bash
pip install numpy pandas matplotlib scipy astropy jupyter


