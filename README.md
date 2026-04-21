# geochemical-data-explorer

A Python-based toolkit for exploratory analysis of geochemical datasets. Designed for geoscientists working with multi-parameter chemical data from rock, soil, or water samples.

---

## Overview

This project provides a structured workflow for loading, cleaning, and statistically analysing geochemical datasets. The toolkit covers descriptive statistics, outlier detection, correlation analysis, and multi-panel visualisation — all implemented using standard scientific Python libraries.

Developed as part of ongoing research in hydrogeology and applied geoscience at Presidency University, Kolkata.

---

## Features

- Descriptive statistics with coefficient of variation (CV%)
- IQR-based outlier detection with per-parameter reporting
- Pearson correlation heatmap
- Frequency distribution histograms (all parameters)
- Grouped boxplots by geochemical classification
- Pairplot with KDE diagonals
- EC vs TDS scatter with linear regression overlay

---

## Project Structure

```
geochemical-data-explorer/
│
├── dataset.csv          # Input geochemical dataset (80 samples, 15 parameters)
├── analysis.py          # Main analysis script
├── outputs/             # Generated plots and CSV reports
│   ├── descriptive_statistics.csv
│   ├── outlier_report.csv
│   ├── correlation_matrix.png
│   ├── histograms.png
│   ├── boxplots_by_watertype.png
│   ├── pairplot.png
│   └── EC_vs_TDS.png
└── README.md
```

---

## Dataset

The dataset contains 80 geochemical samples with the following parameters:

| Category | Parameters |
|---|---|
| Major cations | Ca, Mg, Na, K |
| Major anions | HCO₃, Cl, SO₄, NO₃ |
| Physical | pH, EC (µS/cm), TDS (mg/L), Temp (°C) |
| Derived | TH (Total Hardness) |
| Trace metals | Fe, Mn |
| Classification | WaterType (Ca-HCO₃ / Ca-Cl / Na-HCO₃ / Na-Cl) |

---

## Requirements

```
pandas
numpy
matplotlib
seaborn
scipy
```

Install via:

```bash
pip install pandas numpy matplotlib seaborn scipy
```

---

## Usage

```bash
# Step 1: Generate dataset (or replace with your own CSV)
python dataset.py

# Step 2: Run full analysis
python analysis.py
```

All outputs are saved to the `outputs/` directory.

---

## Sample Outputs

### Correlation Matrix
Shows Pearson correlation coefficients across all 14 parameters. Strong positive correlations observed between EC–TDS and Ca–TH, consistent with expected geochemical relationships.

### Grouped Boxplots
Parameter distributions segmented by water type, highlighting compositional differences between Ca-dominated and Na-dominated facies.

### EC vs TDS Regression
Linear regression confirms strong EC–TDS coupling (R² reported in plot), useful for field estimation of TDS from conductivity measurements.

---

## Geoscience Context

Geochemical data analysis is fundamental to understanding rock–water interaction, diagenetic processes, and hydrochemical evolution. This toolkit is applicable to:

- Groundwater hydrochemistry studies
- Soil and regolith geochemistry
- Mine drainage and acid rock drainage assessment
- Ore deposit geochemistry (preliminary data QC)

---

## Author
Anikate Chowdhury  
ORCID: https://orcid.org/0009-0004-5580-2470

---

## Citation
If you use this methodology or implementation logic in academic or technical work,
please cite this repository. 

DOI: 

