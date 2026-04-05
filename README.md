# Improved Risk Stratification and Prediction of Late Recurrence  
### HR+, HER2− Early Breast Cancer — METABRIC Dataset

**Authors:** Janeeba Ashraf · Revathy S Arun  
**Dataset:** METABRIC (n = 2,509 → 1,025 after filtering)  
**Tools:** R 4.x · survival · survminer · ggplot2  

---

## Project Overview

This bioinformatics project investigates the discordance between 
clinical risk stratification tools and identifies predictors of 
late recurrence (>60 months) in HR+, HER2− early breast cancer 
using the METABRIC clinical dataset.

---

## Research Objectives

1. Quantify discordance between NPI and CTS5 risk classifications
2. Identify predictors of early vs late recurrence using Cox regression
3. Validate NPI as a cost-effective risk stratification tool

---

## Key Findings

| Finding | Result |
|---|---|
| Patients analysed | 1,025 HR+/HER2− Stage I–III |
| NPI vs CTS5 discordance | **86.8%** |
| Late recurrence rate (>60m) | 25.9% (192/742) |
| Early recurrence predictor | PR status — HR = 0.67, p = 0.013 |
| Late recurrence predictor | Lymph nodes only — HR = 1.10, p < 0.001 |
| NPI Low Risk median RFS | 294.8 months |
| NPI High Risk median RFS | 68.2 months |
| Log-rank significance | p < 0.0001 |

---

## Plots

### Late Recurrence-Free Survival by NPI Group
![Late Recurrence KM](plots/plot_LateRecurrence.png)

### Hazard Ratios — Late Recurrence (>60 months)
![Forest Plot Late](plots/plot_ForestLate.png)

### Risk Classification Discordance: NPI vs CTS5
![Discordance Heatmap](plots/plot_Discordance_Heatmap.png)

---

## How to Reproduce

1. Download METABRIC data from [cBioPortal](https://www.cbioportal.org/study/summary?id=brca_metabric)
2. Place `brca_metabric_clinical_data.tsv` in your working directory
3. Open `code/tcga_analysis_complete.R` in RStudio
4. Install packages if needed (lines at top of script)
5. Run the full script — all plots will be generated and saved

---

## Reference

Fasching PA et al. (2024). Identification of Patients with Early  
HR+ HER2− Breast Cancer at High Risk of Recurrence.  
*Geburtshilfe und Frauenheilkunde*, 84: 164–184.  
DOI: 10.1055/a-2238-3199
