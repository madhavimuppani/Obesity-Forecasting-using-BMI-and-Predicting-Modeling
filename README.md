# Obesity-Forecasting-using-BMI-and-Predicting-Modeling
SAS JMP

## Project Overview

This project analyzes the Obesity dataset to predict and understand patterns of obesity based on various factors such as lifestyle, dietary habits, and physical activity. The analysis involves data preprocessing, feature engineering, and the development of multiple predictive models to explore relationships between variables and assess model performance.

---

## Workflow and Methodology

### 1. **Data Preprocessing**
   - The dataset contains various columns, including demographic, lifestyle, and dietary information such as:
     - **Age, Height, Weight, Gender, Obesity levels, Smoking habits, and more**.
   - Key preprocessing steps:
     1. **Calculated BMI**: Derived from height and weight using the formula:  
        \[
        BMI = \frac{\text{Weight (kg)}}{\text{Height (m)}^2}
        \]  
        BMI categories (underweight, healthy, overweight, obese) were derived for further analysis.
     2. **Feature Recoding**:
        - `MTRANS` recoded to group all transportation-related categories into "Transportation."
        - `Obesity` recoded to group various obesity levels into a single category called "Obese."
     3. Split the dataset into training and validation sets using a random seed of `888` for reproducibility.

### 2. **Modeling Approaches**
   - Multiple machine learning models were built to predict BMI and classify obesity levels.

#### **Linear Regression**
   - **Target Variable**: BMI.
   - Dropped features: `Weight`, `Height`, `Obesity` (target leakage), `CALC` (bias), `SMOKE`, `Gender`, `SCC`, and `TUE`.
   - Developed a final model with the selected features.

#### **Logistic Regression**
   - **Target Variable**: Obesity category.
   - Dropped features: `Age`, `NCP`, `SMOKE`, `FAF`, `Obesity 2`, `FCVC`, and `MTRANS 2`.

#### **Decision Tree**
   - Built a decision tree to explore variable importance and relationships.

#### **Bootstrap Forest**
   - Developed a bootstrap forest for robust predictive modeling.

#### **Boosted Tree**
   - Implemented a boosted tree to improve model accuracy through iterative boosting techniques.

#### **Neural Network**
   - Designed a neural network to capture non-linear relationships in the data.

### 3. **Model Comparison**
   - Evaluated and compared the performance of all models based on key metrics such as accuracy, precision, and recall.
   - Provided insights into the most effective model for predicting BMI and obesity classification.

---

## Repository Structure

- **Obesity_Project.jmp**: Contains the processed dataset, modeling steps, and results.
- **README.md**: This file provides an overview of the project and its workflow.

---

## Key Features

- **Feature Engineering**: Calculated BMI and recoded features for better analysis.
- **Predictive Modeling**: Built multiple models, including regression, decision trees, forests, and neural networks.
- **Model Evaluation**: Compared models to determine the best-performing approach for predicting BMI and obesity levels.

---

## Tools and Technologies Used

- **Data Analysis**: JMP for data preprocessing and modeling.
- **Statistical Models**: Linear regression, logistic regression, and decision trees.
- **Machine Learning**: Bootstrap forest, boosted tree, and neural network.

---

## Outcomes

- Identified key features influencing obesity levels.
- Developed a robust predictive framework for BMI and obesity classification.
- Gained insights into the relationships between lifestyle factors and obesity.

---

For further questions or contributions, feel free to open an issue or submit a pull request!
