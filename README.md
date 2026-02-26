# Coronavac Cohort: Indigenous Public Health & Modeling

## Project Context

This repository provides a **Data Reader** and **Visualization Dashboard** for utilizing Indigenous epidemic data, specifically gathered by the Grupo de Pesquisa e . It is designed to bridge the gap between field data collection in Google Sheets and high-level computational social science.

### Scientific Objective: Generative Modeling

The primary intent of this codebase is to process stratified epidemiological data to power **Generative Bayesian SIR (Susceptible-Infectious-Recovered)** models. 

By analyzing incidence across specific intersections of **Village**, **Ethnicity**, and **Household Size** (with more factors to come) we aim to:

* Estimate transmission parameters ($\beta$, $\gamma$) unique to specific communal living structures.
* Infer which set of biological or socio-economic factors best explains the observed data by comparing marginal likelihoods calculated via Bayesian model fitting.
* Account for heterogeneity in vaccine response and contact patterns within Indigenous territories.
* Utilize stratified cumulative incidence curves to inform the likelihood functions of our Bayesian fits.


### The Pipeline Architecture

1. **Indigenous Data Sovereignty:** No sensitive individual-level data is stored here. The `cohort-data.csv` is a synthetic dataset used for model validation.
1. **R Pipeline:** Automatically toggles between Google Sheets API and local CSV backups.
1. **Data interface includes basic visualizations to adapt for research:** Future analyses can include this data interface as a dependency to fetch data from different communities and contexts.

### Dashboard & Visualization

The project includes a Quarto Dashboard that visualizes:

* **Daily and Cumulative Incidence:** Stratified by Village and Ethnicity.
* **Cross-factor visualization:** A facet grid intersection of Village x Household Size x Ethnicity to identify transmission variance.
