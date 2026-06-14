# CSC61304 Group 11: roject Tasks & Overview

## Project Overview
 
This project applies machine learning to predict literacy and educational outcomes in Nepal, using data from the National Population and Housing Census 2021 (NPHC 2021). By analyzing school attendance, literacy status, and educational attainment across Nepal's 753 local levels, we train and compare five ML models to identify at-risk populations and predict literacy outcomes.
 
The findings are intended to support Nepal's Ministry of Education in identifying underserved local levels, targeting literacy programs, and allocating educational resources to reduce dropout rates across the country.
 
## Case Study Track
 
**Track:** Track 4 — ML for Education & Student Success  
**Client:** Nepal Ministry of Education  
**Objective:** To apply machine learning algorithms on Nepal's 2021 Census education data to predict literacy outcomes and identify at-risk populations across Nepal's 753 local levels.
 
## Dataset
 
**Source:** National Statistics Office (NSO) Nepal — National Population and Housing Census 2021  
**Portal:** https://censusresults.nsonepal.gov.np/downloads/census-dataset
 
Three individual-level census tables are merged on common keys (`prov`, `dist`, `gapa`, `sex`, `agegrp`):
 
- **Table 17 (Literacy Status)** — literacy outcome of the population (can read/write, read only, or illiterate)
- **Table 18 (Educational Attainment)** — how far people progressed through the education system (primary, secondary, graduate etc.)
- **Table 19 (School Attendance)** — who is currently attending school, who dropped out, and who never attended
**Rows:** 60,000+  
**Features:** 15–21 after feature selection
 
See `DATASET_DOCUMENTATION.md` for full column details and merging strategy. (Not done yet)

## ML Pipeline

1. Exploratory Data Analysis (EDA)
2. Preprocessing
3. Feature Selection
4. Train Models
5. Evaluate
6. Compare

## GitHub Repository

**Repository:** https://github.com/Prajit208/CSC61304-Group11-ML

## Learn These Git Commands

- `git clone <url>` : download the repo to your computer (do this once)
- `git pull` : get the latest changes from GitHub (do this every session before working)
- `git add notebooks/yourfilename.ipynb` : stage your file for commit
- `git commit -m "your message"` : save your changes locally
- `git push` : upload your changes to GitHub
- `git status` : check what files have been changed

**Rules:**
- Never run `git add .`
- Always `git pull` before starting work
- Only add your own notebook file


## Repository Structure

```
CSC61304-Group11-ML/
│
├── data/
│   └── README.md               # Instructions to download the dataset
│
├── notebooks/
│   ├── 01_EDA.ipynb            # Exploratory Data Analysis
│   ├── 02_preprocessing.ipynb  # Data cleaning, encoding, feature selection
│   ├── 03_random_forest.ipynb  # Random Forest
│   ├── 04_decision_tree.ipynb  # Decision Tree
│   ├── 05_logistic_regression.ipynb  # Logistic Regression
│   ├── 06_naive_bayes.ipynb    # Naive Bayes
│   └── 07_kmeans.ipynb         # K-Means Clustering
│
├── results/
│   └── model_comparison.csv    # Master performance table (all models)
│
├── requirements.txt            # Python dependencies
└── README.md
```

## Task Division

| Task | Assigned To | Description |
|---|---|---|
| EDA | Krish | Exploratory Data Analysis |
| Preprocessing | Prajit | Data cleaning, encoding, feature engineering |
| Model comparison |  | Compile results from each member's model and identify best model |
| Report compilation |  | Compile full report per submission format |
| Meeting minutes |  | Document all meeting logs for appendix |
| Random Forest | Krish | Model training, evaluation, report section |
| Decision Tree | Reha | Model training, evaluation, report section |
| Logistic Regression | | Model training, evaluation, report section |
| Naive Bayes |  | Model training, evaluation, report section |
| K-Means Clustering |  | Model training, evaluation, report section |

## Model Training Requirements

Each member assigned a model must complete the following:

### Literature Review
Research and write about your model in the context of earthquake damage prediction. Include at least 2 references.

### Model Description
- What it does in plain language
- How it works — step-by-step logic and mathematical foundation with formulas
- When to use it — what type of problem it suits
- Strengths and weaknesses

### Implementation
- Load the preprocessed data from `data/processed_data.csv`
- Implement and train your model using scikit-learn


### Results and Evaluation
- Accuracy, Precision, Recall, F1-score, Confusion Matrix
- Explain each metric and identify which matters most for this problem
- Critically analyze and interpret your results

### Conclusion
Summarize key findings from your model — what did it learn, how well did it perform, what are its limitations.

### References
Include at least 2 references in APA format.

### Presentation Slide
Write and design your section of the group presentation slides.

## Requirements

- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- jupyter