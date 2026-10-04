# AI Usage

This project was developed with AI-assisted workflows to accelerate code generation, debugging, verification, and documentation. The primary tools used were GitHub Copilot and the built-in VS Code AI assistance, which were used to support the implementation of the ShiftProof ML pipeline and the supporting project artifacts.

## What the AI was used for

- Requirements understanding: reviewed the project goals, architecture, and expected outputs for the placement predictor workflow.
- Project scaffolding: generated and refined the Python package structure, module layout, and configuration files required to run the app and tests.
- Pipeline development: assisted with data preprocessing, model selection logic, evaluation reporting, and calibration steps.
- Debugging and troubleshooting: helped diagnose issues in the training/evaluation flow, validate failing test cases, and correct implementation mistakes.
- Documentation support: assisted in drafting the project overview, architecture notes, and usage guidance so the repository is easier to understand and run.
- Validation workflow: used to clarify test failures, review edge cases, and confirm that the final behavior matches the intended project design.

## Verification workflow

The project was validated using the repository’s testing workflow and targeted checks:

- Python test suite: `python -m pytest -q`
- Streamlit app launch: `streamlit run app.py`
- Optional API check: `uvicorn shiftproof.api:app --app-dir src --reload`

These checks are intended to confirm that the data pipeline, model artifacts, and app entry points continue to work as expected after code changes.

## AI-assisted development principles used

- Human review remained in control of the final implementation decisions.
- AI suggestions were checked against the project requirements and the actual test results.
- Outputs were validated before being treated as final, especially for model logic and data-processing behavior.
- Documentation and report files were reviewed for correctness and consistency with the codebase.

## Final note

AI tools were used as a productivity and reasoning aid, not as a substitute for engineering judgment. The final repository reflects a code review and validation process that verifies the project works with the expected ML and app workflows.
