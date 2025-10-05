# TasD — Classification Coursework

This repository contains the deliverables for a supervised classification coursework: a Jupyter notebook with the analysis and modeling pipeline, the datasets used, the course specification PDF, and a few experiment artifacts.

Key goals of the coursework
- Explore and preprocess the provided dataset.
- Implement baseline and improved classification approaches.
- Evaluate models using standard metrics and present findings in the notebook.

Repository contents
- `coursework.ipynb` — the main Jupyter notebook. It contains EDA, preprocessing, model training, evaluation, and discussion of results.
- `dataset.json` — original dataset (as provided for the assignment).
- `cleaned_dataset.json` — preprocessing output used by the notebook.
- `val.json` — validation split used for evaluation.
- `Classification Coursework Specification.docx.pdf` — the assignment brief and marking criteria.
- `requirements.txt` — list of Python dependencies required to run the notebook.
- `llm_prompt_template_1.json`, `llm_prompt_template_2.json`, `llm_prompt_template_3.json` — prompt templates used for any LLM-assisted experimentation.

Quick start

1. Create and activate a virtual environment, then install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

2. Launch the notebook server and open `coursework.ipynb`:

```bash
jupyter notebook coursework.ipynb
```

3. The notebook expects the dataset files to be in the repository root. If you move them, update the file paths inside the notebook accordingly.

What you'll find in the notebook
- Exploratory data analysis and basic visualisations.
- Data cleaning and preprocessing steps; tokens, features, or other transforms used for models.
- Baseline classifier(s) (e.g., logistic regression or naive baseline) and at least one improved approach.
- Evaluation: accuracy and per-class F1 (or similar) and a discussion of results and limitations.

Assumptions and notes
- I intentionally kept outputs (model checkpoints, large logs) out of the repository to keep it small. If you reproduce experiments, save large artifacts outside the repo or add them to `.gitignore`.
- The PDF `Classification Coursework Specification.docx.pdf` contains the formal brief. The README is a companion summary, not a substitute for the spec.

Troubleshooting
- If a dependency fails to install, check your Python version (recommended: 3.8+). If necessary, create a fresh virtual environment.
- If the notebook cannot find the data files, ensure `dataset.json` / `cleaned_dataset.json` are in the repo root or update the paths in the notebook.

Reproducibility and extension ideas
- To reproduce results exactly, set random seeds in the notebook cells where models are trained.
- You can add experiments (different feature engineering, different model families) in separate notebook cells or copy the notebook and create a variant.

License and contact
- This repository contains coursework submitted for assessment. If you want to reuse any code, please check with the course guidelines or contact the author by opening an issue.

---

If you'd like, I can extract specific headings or instructions from the attached coursework PDF and add a short summary to this README. I can also produce a short description and a set of topics you can paste into GitHub's About panel.
