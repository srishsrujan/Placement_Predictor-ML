# Placement Predictor ML

A deployed Streamlit-based machine learning application that estimates a student's placement readiness using academic records, aptitude, technical and communication skills, coding practice, projects, internships, certifications, and backlogs.

This project is designed for:
- individual student assessment
- what-if career planning scenarios
- cohort-level analytics across branches and graduation years
- bulk prediction from CSV uploads

## Live demo

Deployed app: https://shiftproof-ml.streamlit.app/

GitHub repository: https://github.com/srishsrujan/Placement_Predictor-ML

This repository powers the deployed placement predictor web app. The project is intended to be used as a practical ML demo and decision-support tool for student planning.

## Features

- Student profile scoring with readiness percentage and category
- Strengths and focus-area recommendations
- Scenario simulation for coding hours, projects, and internships
- Branch and cohort analytics dashboard
- CSV batch prediction workflow
- Model comparison metrics and reporting outputs

## Tech stack

- Python
- Streamlit
- Pandas
- scikit-learn
- NumPy
- Uvicorn (optional API)

## Repository overview

- `app.py` — Streamlit dashboard entry point
- `src/shiftproof/` — ML preprocessing, training, prediction, and reporting logic
- `data/` — generated synthetic student dataset and data utilities
- `reports/` — evaluation reports and metrics
- `artifacts/` — saved trained model assets
- `tests/` — automated validation tests
- `sample_input.csv` — example CSV for batch predictions

## Local setup

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python scripts/generate_and_train.py
streamlit run app.py
```

Optional API:

```powershell
uvicorn shiftproof.api:app --app-dir src --reload
```

Run tests:

```powershell
python -m pytest -q
```

## Data and model notes

The project uses a synthetic dataset generated for demonstration purposes. The target field `placement_ready` represents a training label derived from an example outcome process and should not be interpreted as a real-world hiring prediction or guarantee.

The pipeline includes:
- missing-value handling
- feature scaling
- categorical encoding
- comparison of multiple models
- final model selection and calibration on validation data

## Important disclaimer

This tool is meant for educational and planning use. Predictions are informative only and should not replace real placement decisions, recruiter judgment, or validated institutional data.

## Outputs

Training generates model artifacts and analysis reports under:
- `artifacts/`
- `reports/`

These include model comparison summaries, calibration outputs, and cohort-level evaluation metrics.
