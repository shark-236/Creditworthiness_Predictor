# Module_12_Challenge
Repository housing Module 12 Challenge code and supporting documents.

---

## Overview of the Analysis

The purpose of this analysis is to build a model that can identify the creditworthiness of borrowers applying for loans. The model will make use of a dataset containing historical lending activity provided by a peer-to-peer lending services company.   

The data, provided in this repository under the "Resources" folder, contains financial information for loans. Each loan is further detailed by the following descriptive aspects: loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt, and loan status (where 0 = healthy and 1 = unhealthy). Once this data is fed into our learning model, trained, and tested, we will use the model to attempt to predict the creditworthiness of new applicants. These predictions will be captured in a variable called 'value_counts' which will denote the sum of healthy and unhealthy loans predicted. Once compared to testing data, we will be able to infer the model's accuracy in the predicted status versus the actual reported status.  

To create the model we first split the financial information data into 'training sets' and 'testing sets'. The training data teaches the model, and the testing data is used to measure the model's efficacy. The model used is a Logistic Regression which will predict numerical values. Numerical values to predict in this analysis are the binary '0' or '1', alluding to healthy or unhealthy loans respectively. During the implementation of the model we find that the training data is skewed towards healthy loans (as there are many more healthy loans in the data as compared to the quantity of unhealthy loans). To combat this skew, we create a second model with "oversampled" data, which allows us to balance the data with more instances of unhealthy loans to healthy loans. After both models are built and tested, we will compare their predictive efficacy through classification reports.  

---

## Results  

Model 1: Data unaltered, split into training and testing sets. All scores are rounded to two decimal points. 
-Accuracy Score: 0.95. This model correctly predicted the results 95% of the time. This includes True Healthy loans, False Healthy loans, True Unhealthy loans, and Fale Unhealthy loans.  
-Precision Score: 1.00 for '0' prediction ('healthy'), 0.85 for '1' prediction ('unhealthy'). Average of 0.99 overall (remember, this used imbalanced data). The precision is the measure of the model correctly predicting True Healthy loans (versus False Healthy loans).  
-Recall Score: 0.99 for '0' prediction ('healthy'), and 0.91 for '1' prediction ('unhealthy'). Average of 0.99 overall. The recall is the measure of the model correctly predicting True Unhealthy loans (versus False Unhealthy loans).  

Model 2: Oversampled data, split into training and testing sets.  
-Accuracy Score: 0.99. This model correctly predicted the results 99% of the time. This includes True Healthy loans, False Healthy loans, True Unhealthy loans, and False Unhealthy loans.  
-Precision Score: 1.00 for '0' prediction ('healthy'), 0.84 for '1' prediction ('unhealthy'). Average of 0.99 overall. The precision is the measure of the model correctly predicting True Healthy loans (versus False Healthy loans).  
-Recall Score: 0.99 for '0' prediction ('healthy') and 0.99 for '1' prediction ('unhealthy'). Average of 0.99 overall. The recall is the measure of the model correctly predicting True Unhealthy loans (versus False Unhealthy loans). 

---

## Summary

Both of the models performed well. However, for this analysis we are primarily interested in the classification of the Unhealthy loans. As such, Model 2 outperforms Model 1 in this regard. With a higher Recall Score, Model 2 is better at predicting the True Unhealthy loans. In other words, Model 2 classifies Unhealthy loans to a higher success rate than Model 1. 

---

## Technologies

This program uses the following packages:  
Python 3.9.13   
Pandas 1.4.4  
NumPy 1.21.5  
scikit-learn 1.0.2  
imbalance-learn 0.10.1  

---

## Installation Guide 

To check your current package versions, run the following code in your terminal:  
python --version  
pip show pandas  
pip show numpy  
conda list scikit  
conda list imbalanced-learn 

If installation of these packages is required, run the following code:  
conda install pandas  
pip install numpy  
pip install -U scikit-learn   
conda install -c conda-forge imbalanced-learn    

---

## Usage

Important: This program is intended purely for academic purposes, and is solely an example of what is possible. This repository, program, and relevant files are not intended to provide actual analysis advice.   

To begin using this program, please download the following files (included in this repository) to your local machine:  
credit_risk_resampling.ipynb  
lending_data.csv (included in the 'Resources' folder of this repository)  

Running the first cell will import the required packages. The following cells will call in the information from the CSV file (note: you may need to modify the folder path depending on where the CSV was saved). The code will convert the CSV files into DataFrames. Continue on to run the Regression analysis and classification reports. 

---

## Contributors

Shahrukh Alam

---

## License

Columbia Engineering: FinTech Bootcamp