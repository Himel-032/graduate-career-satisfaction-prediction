# Graduate Career Satisfaction Prediction

A machine learning project focused on predicting graduate career satisfaction using survey data from recent graduates and early-career professionals. The repository compares multiple supervised classification models to assess which approach best predicts satisfaction levels based on education, career experience, domain transition, and professional development factors.

## Project Overview

This project analyzes a graduate career survey and builds classification models for:

- 3-class satisfaction prediction: Low, Medium, High
- 5-class satisfaction prediction: original 1–5 rating levels

The aim is to understand which factors are most associated with career satisfaction and to benchmark several common machine learning algorithms on the same dataset.

## Motivation

Career satisfaction is influenced by many factors, including:

- academic experience
- university support and learning environment
- internships and practical training
- technical skills and project experience
- career domain alignment
- future career intent and domain shift
- AI adoption and perceived usefulness

By modeling these features, the project provides a structured way to evaluate how educational and career experiences relate to career outcomes.

## Dataset

The project uses survey-based data with graduate responses and a range of categorical and numerical features. The raw data is processed and transformed into a supervised learning dataset for classification tasks.

Included dataset artifacts:

- 3_Class_Classification/career_satisfaction_3class_processed.csv
- 3_Class_Classification/career_satisfaction_3class_weka.arff
- 5_Class_Classification/career_satisfaction_5class_processed.csv
- 5_Class_Classification/career_satisfaction_5class_weka.arff

## Repository Structure

```text
graduate-career-satisfaction-prediction/
├── README.md
├── 3_Class_Classification/
│   ├── classification_3_class.ipynb
│   ├── career_satisfaction_3class_processed.csv
│   ├── career_satisfaction_3class_weka.arff
│   ├── Figures/
│   ├── Weka-Log/
│   └── weka-models/
│       ├── 5-Fold-Stratified-Cross-Validation/
│       └── 80_Percent_training_20_Testing/
├── 5_Class_Classification/
│   ├── classification_5_class.ipynb
│   ├── career_satisfaction_5class_processed.csv
│   ├── career_satisfaction_5class_weka.arff
│   ├── Figures/
│   └── weka-results/
└── .gitignore
```

## Methodology

The notebooks follow a standard machine learning workflow:

1. Load and inspect the survey dataset
2. Clean and preprocess the dataset
3. Engineer features such as years since graduation, domain switch indicators, and academic support signals
4. Remove irrelevant or noisy columns
5. Split data into training and testing sets
6. Apply preprocessing pipelines using scaling and one-hot encoding
7. Train multiple classifiers
8. Evaluate using cross-validation and holdout testing
9. Compare performance using metrics such as accuracy, precision, recall, F1-score, and confusion matrix analysis
10. Export processed datasets for use with WEKA or further analysis

## Models Evaluated

The experiments benchmark several supervised classification models, including:

- Decision Tree
- Gradient Boosting
- k-Nearest Neighbors
- Logistic Regression
- Multi-Layer Perceptron
- Naive Bayes
- Random Forest
- Ridge Classifier
- Support Vector Machine (RBF)

## Evaluation Strategy

The project uses:

- stratified train-test split
- 5-fold stratified cross-validation
- model comparison across multiple metrics
- confusion matrix analysis
- feature importance inspection for key predictors

## Requirements

Python environment with the following packages:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- openpyxl
- jupyter

## Setup

Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate   # Linux/macOS
.venv\Scripts\activate      # Windows
```

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

## Usage

Open the notebooks in Jupyter:

```bash
jupyter notebook
```

Then explore:

- 3_Class_Classification/classification_3_class.ipynb
- 5_Class_Classification/classification_5_class.ipynb

## Key Insights Provided by the Project

The project investigates how factors such as:

- domain change intentions
- academic support
- extracurricular participation
- career domain alignment
- experience and graduation timeline

can influence graduate satisfaction. It also compares how different classifiers perform on the same survey dataset.

## Notes

- Some model files and structured results are stored under the classification folders for benchmarking and reproducibility.
- The project is suitable for academic or research-oriented experimentation in prediction and classification.
- Some cleaned outputs are exported in CSV and ARFF formats for compatibility with WEKA workflows.

## License

This project is intended for academic and research use. Please check the repository owner or institution policies before reusing the dataset or publishing derived work.

## Acknowledgements

This work is based on graduate survey data and machine learning experimentation. It is designed to support learning, benchmarking, and understanding of the relationship between graduate experiences and career satisfaction.
