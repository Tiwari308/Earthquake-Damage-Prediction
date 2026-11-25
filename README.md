# Earthquake Damage Prediction

## Project Overview

This project uses machine learning to predict the level of earthquake damage to buildings based on their geographical, structural, and building-related characteristics.

The objective is to classify buildings into three damage grades:

- **Grade 1:** Low Damage
- **Grade 2:** Medium Damage
- **Grade 3:** Severe Damage (Almost Complete Destruction)

## Dataset

The project uses the Nepal earthquake building damage dataset, containing 260,601 building records and 38 input features after excluding the building ID.

The dataset includes geographical information, building age, number of floors, building area, height, structural characteristics, and other building attributes.

Dataset files are not included in this repository unless redistribution is permitted by their applicable terms.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- XGBoost
- Joblib

## Project Workflow

1. Data loading and merging
2. Data cleaning and preprocessing
3. Exploratory Data Analysis (EDA)
4. Numerical and categorical feature analysis
5. Geographic analysis
6. Categorical feature encoding
7. Train-validation-test splitting
8. Model training and comparison
9. Hyperparameter experimentation
10. Final model evaluation
11. Feature importance analysis
12. Prediction probability analysis

## Machine Learning Models

The following classification models were evaluated:

- Decision Tree
- Random Forest
- Extra Trees
- XGBoost

XGBoost was selected as the final model based on its overall validation performance.

## Final Model Performance

| Metric | Test Result |
|---|---:|
| Accuracy | 66.20% |
| Macro F1-score | 63.81% |
| Weighted F1-score | 66.79% |
| Mean Absolute Error | 0.3520 |

The model achieved a Grade 3 recall of approximately 72%.

**Evaluation note:** The test dataset was also used in preliminary baseline and tree-model experiments before the final evaluation. Therefore, the final test results should not be considered a completely untouched holdout estimate.

## Repository Structure

```text
Earthquake-Damage-Prediction/
├── dataset/
├── notebooks/
│   └── Earthquake_Damage_Analysis.ipynb
├── models/
│   ├── earthquake_xgboost_model.pkl
│   ├── earthquake_preprocessor.pkl
│   └── model_metadata.json
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run the Project

1. Clone this repository.
2. Create and activate a Python virtual environment.
3. Install the required packages using `pip install -r requirements.txt`.
4. Place the permitted dataset files in the `dataset/` folder.
5. Open `notebooks/Earthquake_Damage_Analysis.ipynb` in Jupyter Notebook or VS Code.
6. Run the notebook cells.

## Limitations

- The model's predictions are not a replacement for professional structural inspections.
- Grade 2 and Grade 3 damage are sometimes confused by the classifier.
- Prediction probabilities are model outputs and are not necessarily calibrated real-world confidence estimates.
- Geographic and structural associations in this dataset should not be interpreted as proof of causation.

## Future Improvements

- Improve identification of severely damaged buildings.
- Explore ordinal classification methods.
- Perform probability calibration.
- Evaluate the model on an independent external dataset.
- Explore additional geographic and seismic risk information.

## Author

**Abhishek Tiwari**

GitHub: [Tiwari308](https://github.com/Tiwari308)
