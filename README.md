# Multi-Class_Obesity_Risk_Prediction
View HTML file: [File](../obesity-risk-prediction.html)

This project utilizes Machine Learning to predict an individual's obesity risk level based on their physical characteristics, dietary habits, and lifestyle choices.

## Project Overview
The goal of this project is to perform multi-class classification on the `NObeyesdad` variable. The model categorizes individuals into different weight-related classes, such as:
* Insufficient Weight
* Normal Weight
* Overweight Level I & II
* Obesity Type I, II, & III

## Dataset Features
The model is trained on various features:
- **Demographics**: Gender, Age, Height, Weight.
- **Family History**: `family_history_with_overweight`.
- **Dietary Habits**: `FAVC` (High caloric food consumption), `FCVC` (Vegetable consumption), `NCP` (Number of meals), `CAEC` (Snacking habits), `CH2O` (Daily water intake).
- **Lifestyle/Physical Activity**: `SMOKE`, `SCC` (Calorie monitoring), `FAF` (Physical activity frequency), `TUE` (Technology usage time), `CALC` (Alcohol consumption), `MTRANS` (Mode of transportation).

## Technologies Used
- **Python**: Primary programming language.
- **Pandas**: For data manipulation and analysis.
- **Scikit-Learn**: Used for data preprocessing (`LabelEncoder`) and model evaluation.
- **XGBoost**: Implementation of the `XGBClassifier` for gradient-boosted decision trees.
- **Matplotlib**: For visualizing feature distributions and encoding results.

## Project Workflow
1.  **Data Acquisition**: Loading training and testing datasets from CSV files (`obesity_train.csv`, `obesity_test.csv`).
2.  **Preprocessing**: 
    - Creating data copies to maintain original integrity.
    - Encoding categorical variables into numerical format using `LabelEncoder`.
3.  **Exploratory Data Analysis (EDA)**: Visualizing encoded values and analyzing feature correlations.
4.  **Modeling**: Training an `XGBClassifier` specifically tuned for multi-class classification.
5.  **Evaluation & Prediction**:
    - Predicting risk levels for the test set.
    - Generating a final submission file containing the `id` and predicted `NObeyesdad` class.

## Setup & Installation
To run this project locally, ensure you have Python installed along with the required libraries:

```bash
pip install pandas scikit-learn xgboost matplotlib
