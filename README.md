# LendingClub Loan Default Prediction

**Goal**  
Predict whether a borrower will default (Charged Off) or fully repay using only pre-loan features.  
We optimize for catching more defaults (higher recall) and choose a probability threshold accordingly.

## Dataset

Download the **LendingClub Accepted Loans 2007–2018Q4** dataset from Kaggle:  https://www.kaggle.com/wordsforthewise/lending-club
File used: `accepted_2007_to_2018q4.csv.gz` (large; not in this repo).

## Project Structure
.
├── config/
│   ├── config.yaml
│   └── feature_info.json
├── data/              # empty in git (no data committed)
├── models/            # created locally by 06 (not committed)
├── notebooks/
│   ├── 01_load_data.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_EDA.ipynb
│   ├── 05_data_pre_processing.ipynb
│   ├── 06_modelling.ipynb
│   └── 07_Summary.ipynb
├── requirements.txt
├── .gitignore
└── README.md

## How to run

1. Create environment
   ```bash
   pip install -r requirements.txt
2. Download dataset from the link above
3. Edit config at config/config.yaml → set data_path to your local file path.
4. Run notebooks in order from the notebooks/ folder:
01 → 02 → 03 → 04 → 05 → 06 → 07
05 saves processed arrays + preprocessor
06 trains & tunes the model and saves best model + threshold
07 reloads artifacts and prints final metrics/plots