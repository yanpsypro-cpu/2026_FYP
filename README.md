# FYP
Final Year Project analysing the impact of COVID-19 on crime patterns across Chicago's 77 community areas (2001–2025).

## Notebooks

| # | Notebook | Description |
|---|----------|-------------|
| 01 | `01_data_acquisition` | Data pull from Chicago Data Portal via Socrata API, cleaning |
| 02 | `02_spatiotemporal_eda` | Temporal trends, seasonal patterns, spatial EDA |
| 03 | `03_spatial_autocorrelation` | Global/Local Moran's I, LISA clusters, Getis-Ord Gi* |
| 04a | `04a_panel_construction` | Build community-area × day panel with crime type decomposition |
| 04b | `04b_data_integration` | Merge mobility, COVID, unemployment, weather data |
| 05a | `05a_causal_inference_did` | Difference-in-Differences with community fixed effects |
| 05b | `05b_synthetic_control` | Synthetic Control Method robustness check |
| 06  | `06_forecasting_xgboost` | XGBoost rolling-window forecasting, SHAP analysis |
| 06b | `06b_causal_forecasting_bridge` | Forecasting–DID bridge across grouping methods |
| 07a | `07a_sensitivity_analysis` | 7-method grouping sensitivity, leave-one-out |
| 07b | `07b_robustness_twfe` | Two-Way Fixed Effects, heterogeneity, triangulation |
| 07c | `07c_temporal_window` | Temporal window sensitivity |
| 07d | `07d_lisa_category` | LISA category specification sensitivity |

## Notes

The thesis reports results from all notebooks, but not all analyses appear in the main text. The core analytical pipeline (data acquisition, EDA, spatial autocorrelation, panel construction, DID causal inference, and sensitivity analysis) is reported in Chapters 3–4. The synthetic control analysis (`05b`), XGBoost forecasting and concept drift detection (`06`), and the causal–forecasting bridge (`06b`) are reported in the appendix as supplementary robustness and exploratory analyses rather than as part of the main argument.

## Data Sources


https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2

https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Community-Areas-current-/cauq-8yn6

https://www.google.com/covid19/mobility/

https://data.cityofchicago.org/Health-Human-Services/COVID-19-Daily-Cases-Deaths-and-Hospitalizations-H/naz8-j4nc

https://www.bls.gov/lau/
## Setup

Python 3.10+

```bash
pip install pandas numpy matplotlib seaborn geopandas libpysal esda splot spreg giddy mapclassify statsmodels scipy xgboost scikit-learn shap sodapy pyarrow
```
