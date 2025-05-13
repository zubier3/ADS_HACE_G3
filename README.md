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

## Datasets

Datasets are private and owned by HACE. Therefore acess to these must be requested

## Requirements

This project uses a Conda environment to manage dependencies. The required packages are specified in the environment.yml file.

Main libraries used:
- `pandas`
- `scikit-learn`
- `spacy`
- `nltk`
- `matplotlib` / `seaborn`
- `xgboost`
- `tqdm`

## Environment Setup

1.  Ensure [Conda](https://docs.conda.io/en/latest/) is installed (e.g., via Miniconda or Anaconda).
2.  Clone this repository:

    ```bash
    git clone [https://github.com/zubier3/ADS_HACE_G3.git](https://github.com/zubier3/ADS_HACE_G3.git)
    cd ADS_HACE_G3
    ```
3.  Create the Conda environment from the `environment.yml` file:

    ```bash
    conda env create -f environment.yml
    ```
4.  Activate the environment:

    ```bash
    conda activate ads_hace_g3
    ```
5.  Install required NLTK data:

    ```python
    import nltk
    nltk.download('punkt')
    nltk.download('punkt_tab')
    nltk.download('stopwords')
    nltk.download('wordnet')
    ```
6.  Install the SpaCy language model (e.g., English small model):

    ```bash
    python -m spacy download en_core_web_sm
    ```

## Running the Project

Open JupyterLab or VS Code with the `ads_hace_g3` environment activated. Run the notebooks in the following order:

1.  `01_02_Preprocessing_EDA.ipynb`
2.  `03_Context_Classifier.ipynb`
3.  `04_Company_Scoring(i).ipynb`
4.  `04_Company_Scoring(ii).ipynb`
5.  `04_Company_Scoring(iii).ipynb`

Ensure access to the HACE datasets before running the notebooks, as they are required for data processing.
