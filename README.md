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

# Classification Coursework — TaD

This repository contains my completed submission for the Text-as-Data (TaD) multi-class classification coursework. The project centers on building, evaluating, and analyzing text classifiers for museum records, following a structured set of tasks and questions.

## What I Did and Achieved

### 1. Data Cleaning & Preparation
- Downloaded and loaded the provided dataset of museum records.
- Identified and fixed issues in the training split, including:
  - Standardizing content and label keys.
  - Removing entries with missing or invalid data.
  - Fuzzy-matching labels to ensure consistency.
- Saved the cleaned dataset as `cleaned_dataset.json` for further analysis.

### 2. Exploratory Data Analysis (EDA)
- Reported sample counts and percentage splits for training, validation, and test sets.
- Calculated minimum and maximum text lengths for each split.
- Identified the five most frequent tokens per class using spaCy tokenization.

### 3. Prompting Large Language Models (LLMs)
- Evaluated three different prompt templates with Llama-3.1-8B-Instruct for record classification.
- Calculated accuracy, macro precision, recall, and F1 for each template.
- Handled invalid LLM outputs as a sixth class and commented on results.

### 4. Fine-tuning Transformer Models
- Fine-tuned a BERT-base transformer using HuggingFace Trainer with specified hyperparameters (8 epochs, lr=5e-5, batch size=8).
- Evaluated the model on the validation set, reporting per-class and macro metrics.

### 5. Validation Set Issue & Fix
- Diagnosed poor validation performance using a confusion matrix.
- Identified and fixed a problem in the validation set, improving model results.

### 6. Hyperparameter Tuning & Model Comparison
- Trained and evaluated four transformer models: BERT, RoBERTa, DistilBERT, BiomedBERT.
- Used `load_best_model_at_end` to select the best checkpoint for each.
- Compared models using accuracy, macro precision, recall, and F1.

### 7. Final Evaluation & Deployment
- Loaded the best-performing model and evaluated it on the test set using a text-classification pipeline.
- Reported per-class and macro metrics, and discussed deployment suitability for the client.

### 8. Generative AI Usage
- Documented any use of generative AI tools in the assignment, as required.

## Repository Contents

- `coursework.ipynb` — Main notebook with code, analysis, and answers.
- `dataset.json` — Original dataset.
- `cleaned_dataset.json` — Cleaned dataset after preprocessing.
- `val.json` — Validation split.
- `llm_prompt_template_1.json`, `llm_prompt_template_2.json`, `llm_prompt_template_3.json` — LLM prompt templates and results.
- `requirements.txt` — Python dependencies.
- `Classification Coursework Specification.docx.pdf` — Assignment brief and marking criteria.

## How to Run

1. Create and activate a Python virtual environment:
	```bash
	python -m venv .venv
	source .venv/bin/activate
	pip install -r requirements.txt
	```
2. Launch Jupyter Notebook:
	```bash
	jupyter notebook coursework.ipynb
	```
3. Ensure all dataset files are in the repository root. Update notebook paths if needed.

## Notes
- Large outputs and model checkpoints are not included to keep the repo small.
- For reproducibility, set random seeds in modeling cells.
- See the assignment PDF for full details and marking criteria.

## License & Contact
This repository is coursework submitted for assessment. For reuse or questions, please open an issue or consult the course guidelines.
