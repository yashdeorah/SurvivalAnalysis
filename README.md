# SurvivalAnalysis

Survival analysis of lung cancer patient data using Kaplan-Meier estimation, log-rank testing, and Cox proportional hazards regression.

## Overview

Exploratory survival analysis built in Python with the [lifelines](https://lifelines.readthedocs.io/) library. The main notebook walks through:

- Exploration of survival times and censoring status
- Kaplan-Meier survival curves, overall and stratified by sex
- A log-rank test comparing survival between groups
- Cox proportional hazards regression on age, sex, and ECOG performance score (`ph.ecog`)
- Proportional hazards assumption checks via `check_assumptions`

## Data

The analysis uses the NCCTG lung cancer dataset bundled with lifelines (`lifelines.datasets.load_lung()`), so no external data download is required. Key fields: `time` (survival time in days), `status` (censoring indicator), `age`, `sex`, and `ph.ecog` (ECOG performance score).

## Project structure

- `notebooks/01_data_exploration.ipynb` - main analysis notebook
- `src/` - package directory for reusable code (currently a stub)
- `requirements.txt` - Python dependencies

## Setup

```bash
python -m venv .venv
source .venv/bin/activate  # on Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Running

```bash
jupyter notebook notebooks/01_data_exploration.ipynb
```

(or `jupyter lab`) and run the cells top to bottom.

## Dependencies

lifelines, pandas, numpy, matplotlib, scipy, jinja2
