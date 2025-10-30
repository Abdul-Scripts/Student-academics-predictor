# Student-academics-predictor
An interpretable ML data product (Jupyter/Colab) that predicts student exam scores from study, attendance, sleep, and prior performance. Flags at-risk students in order to prioritize them for educational assistance.

This project is a Jupyter notebook that predicts **student exam scores** from a few simple inputs:

- hours studied
- sleep hours
- attendance %
- previous scores

It then **flags at-risk students** (those predicted to score below a data-driven threshold) and gives advisors a **triage list** and a small in-notebook **dashboard**.

---

## What it does

- Loads the Kaggle dataset **“Analyzing Student Academic Trends.”**
- Cleans and explores the data (histograms, boxplots, correlations).
- Trains a simple, explainable model (Linear / Ridge).
- Calibrates an **at-risk threshold** (by default: bottom 25% of the cohort).
- Exports an **advisor triage** CSV (masked IDs by default).
- Shows a **dashboard** with:
  - feature importance (bar)
  - exam score by attendance band (box)
  - hours studied vs predicted score (scatter)
- Logs runs and does a light **drift check**.

---

## Why it’s useful

- Identifies students who need help the most
- Identify what variablse are causing student to struggle
- Experiment with variables to plan and see what can help specific students
- Advisors can see **who to advise first**.
- The model is **transparent** (not a black box).
- It works in a **single notebook** (easy to share, easy to grade).

---

## How to run (local)

## You can either view the non-interactive version on github, or view the full notebook with interactive tools by running it locally or via Colab.

### To run locally:

Clone the repo:
   ```
   git clone https://github.com/<your-username>/student-success-data-product.git
   cd student-success-data-product
   ```

Create a virtual env and install:
```
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt  # or install deps below
```

If you don’t have requirements.txt, run:
```
pip install jupyter pandas numpy scikit-learn matplotlib plotly ipywidgets scipy joblib kagglehub
```

Run Jupyter and open the notebook:
```
jupyter notebook
```

### To run via Colab, download the interactive version of the notebook and open it through google colab.

# Dataset

This notebook uses:

Yaseen, S. A. “Analyzing Student Academic Trends.” Kaggle.
Download from: https://www.kaggle.com/datasets/saadaliyaseen/analyzing-student-academic-trends
Note: The data stays under the Kaggle terms. It is not re-licensed here.
