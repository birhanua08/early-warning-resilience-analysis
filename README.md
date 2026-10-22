# Social Protection and Household Food-Security Vulnerability under Compound Shocks

Python analysis workflow for a study examining how PSNP participation, compound shock
exposure, and household resilience capacities are associated with food insecurity among
1,939 agricultural households in four highland woredas of Amhara Region, Ethiopia.

## Related Manuscript
**Social Protection and Household Food-Security Vulnerability under Compound Shocks:  
Evidence from Highland Livelihood Zones in Amhara, Ethiopia**  
Author: Birhanu Ayalew Teka  
Target journal: *Food Policy*

## Study Focus
The analysis examines:
- The relationship between compound shocks and household food insecurity.
- The protective association between PSNP participation and food insecurity.
- Spatial heterogeneity in PSNP effects across districts.
- The use of household assets, geographic access, altitude, and support measures as
  vulnerability and resilience indicators.

## Data
The study uses household survey data from Tach Gayint, Sahila, Sedie Muja, and Meketwa
woredas in South Gondar and Wag Himra zones. GPS coordinates were recorded for 1,933
households.

**Confidentiality note:** Raw household survey data and precise household GPS coordinates
are not shared in this repository. A de-identified or synthetic sample dataset may be
included to illustrate the workflow.

## Analytical Components
- Data cleaning and correction of asset-index placeholder codes.
- Construction of a PCA-weighted household asset index.
- Construction of a direct informal-assistance indicator.
- Descriptive analysis of compound-shock exposure and food insecurity.
- OLS and regularized Random Forest models.
- Kebele-grouped cross-validation for predictive performance.
- Multilevel district-by-PSNP interaction model with cluster-robust standard errors.
- Exploratory ridge-regularized GWR and spatial cross-validation diagnostics.
- Mapping and visualization of household locations and spatial patterns.

## Main Analytical Finding
PSNP participation is associated with significantly lower food insecurity in Meketwa,
while the association is attenuated and statistically indistinguishable from zero in
Sedie Muja. The study therefore supports district-differentiated social-protection
planning rather than fine-grained spatial interpolation.

## Technologies
- Python
- Pandas
- NumPy
- GeoPandas
- scikit-learn
- XGBoost
- Statsmodels
- Matplotlib
- PostGIS / spatial data processing
- Jupyter Notebook

## Repository Structure
```text
├── README.md
├── requirements.txt
├── data/
│   └── sample_data.csv
├── notebooks/
│   └── 01_analysis.ipynb
├── src/
│   ├── 01_data_cleaning.py
│   ├── 02_variable_construction.py
│   ├── 03_descriptive_analysis.py
│   ├── 04_machine_learning.py
│   ├── 05_spatial_analysis.py
│   └── 06_figures_tables.py
├── outputs/
│   ├── figures/
│   └── tables/
└── .gitignore
```

## How to Run
```bash
pip install -r requirements.txt
```

Run the Jupyter notebook or execute the Python scripts in the `src/` folder.

## Outputs
- Cleaned analysis dataset.
- Vulnerability and asset-index tables.
- Model-performance results.
- Multilevel PSNP interaction estimates.
- Maps and figures illustrating spatial patterns.
