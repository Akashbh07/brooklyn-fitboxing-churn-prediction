# Brooklyn Fitboxing: Predicting Member Churn

This project is developed as part of the individual coursework for the module **M516 Business Project in Big Data & AI** at **GISMA University of Applied Sciences**.

The project implements an end-to-end machine learning pipeline to predict member churn at Brooklyn Fitboxing. The aim is to identify members who may be at risk of leaving and provide useful insights that could support proactive retention strategies.

> **Note:** The dataset used in this project is synthetic and is created to simulate member behaviour. Therefore, the model results should not be considered representative of real Brooklyn Fitboxing members.

## Project Structure

* `fitboxing_churn_dataset.csv` – The synthetic dataset containing member demographics, attendance metrics, membership information, and behavioural trends.
* `M516_Final.ipynb` – The main Jupyter Notebook containing data exploration, preprocessing, model training, evaluation, feature importance analysis, and churn probability predictions.
* `README.md` – Project documentation and setup information.

## Machine Learning Approach

The project follows these main steps:

1. Load and explore the dataset.
2. Check the data for missing values and understand the churn distribution.
3. Remove identifying fields such as member ID and full name.
4. Preprocess numerical and categorical features.
5. Split the data into training and testing sets using an 80/20 stratified split.
6. Train and compare two machine learning models:

   * Logistic Regression
   * Random Forest
7. Evaluate the models using accuracy, precision, recall, F1-score, and ROC-AUC.
8. Analyse feature importance using the Random Forest model.
9. Generate churn probabilities for individual members.

## Model Results

The models were evaluated on the test dataset.

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | -------: | --------: | -----: | -------: | ------: |
| Logistic Regression |    72.0% |     0.631 |  0.679 |    0.654 |   0.799 |
| Random Forest       |    73.0% |     0.688 |  0.564 |    0.620 |   0.812 |

The Random Forest model achieved a ROC-AUC of **0.812** on the test data.

## Key Features

The Random Forest feature importance analysis identified several important predictors of churn. The three highest-ranked features were:

* **Days since last visit:** 27.6%
* **Average weekly attendance:** 19.4%
* **Average points per session:** 14.5%

These results indicate that recent visits and member activity are important signals within this synthetic dataset.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook / Google Colab

## Project Links

**GitHub Repository:**
https://github.com/Akashbh07/brooklyn-fitboxing-churn-prediction/tree/main

**Video Demonstration:**
https://1drv.ms/v/c/9707b88a5b987bbe/IQC9K5JR3DfxRKmpMdSWxPTSAc8xRDOVUby4cqBsxEJP68Y?e=fAyoUy

## Future Work

Future improvements could include using real member data and adding additional information such as payment history, member feedback, and longer-term behavioural data. A dashboard could also be developed to make the churn predictions easier for management to monitor and use.

## Author

**Akash Bhadauria**
M516 Business Project in Big Data & AI
GISMA University of Applied Sciences
