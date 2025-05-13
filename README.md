# ADS_HACE_G3: NLP Pipeline for Child Labour Risk Detection in Governance Disclosures

This repository contains the code and notebooks developed for the Applied Data Science group project in collaboration with **HACE: Data Changing Child Labour**. The goal of the project is to detect and assess references to goods associated with child labour in corporate governance disclosures using natural language processing (NLP).

---

## Repository Structure

| Notebook | Description |
|----------|-------------|
| `01_02_Preprocessing_EDA.ipynb` | Preprocessing of governance documents and exploratory data analysis. This includes cleaning text, tokenisation, lemmatisation, and visualisation of goods mentions. |
| `03_Context_Classifier.ipynb` | Development and evaluation of a supervised machine learning model to classify the contextual relevance of ambiguous goods mentions (e.g., "gold"). |
| `04_Company_Scoring(i).ipynb` | Step 1 of company-level scoring: aggregating detected relevant goods mentions and associating them with company names. |
| `04_Company_Scoring(ii).ipynb` | Step 2: refining entity matches, resolving duplicates, and cleaning references across documents. |
| `04_Company_Scoring(iii).ipynb` | Final scoring logic: generating risk indicators and summary tables per company based on detected mentions. |

---

## Requirements

Install the required Python packages using:

```bash
pip install -r requirements.txt
```

Main libraries used:
- `pandas`
- `scikit-learn`
- `spacy`
- `nltk`
- `matplotlib` / `seaborn`
- `xgboost`
- `tqdm`

---

## Running the Project

Open each notebook in the recommended order (from `01_02_Preprocessing_EDA.ipynb` to `04_Company_Scoring(iii).ipynb`) using JupyterLab or VS Code.

---
