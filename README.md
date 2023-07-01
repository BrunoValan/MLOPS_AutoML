# AutoML using Azure's Machine Learning Studio
This is a repository for my second project in my course AIPI 561 - MLOps. The goal of this unit was to familiarize ourselves and begin to use some of the AutoML tools. 
For my project I decided to work with Azure's Machine Learning Studio. This repo will be relatively simple as Machine Learning Studio is a low code/no code AutoML solution. 
The instructions for running the project are here in the read me and the data set that I used (a kaggle data set that uses medical information to predict heart disease is in the 
data directory. 

---

## Data 
Our data set comes from kaggle and can be accessed [here]([url](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)). The data comes from 270 de-identified patients. It contains various information about there health status as well as whether or not they have heart disease. Specifically, the data contained 13 different predictors including
- Age, Sex, Chest Pain, BP, Cholesterol, FBS over 120, EKG Result, Max HR, Excercise angina, ST depression, Slope of ST, Number of vessels seen on flouroscopy, Thallium

The data can be found in this repository under the data directory. Feel free to download and play around with it!


## Modeling 
Our modeling task is a binary classification that aims to predict the presence or absence of heart disease. Overall the Azure ML Studio did a great job. I especially enjoyed the robustness of the output metrics that you can look through. You can see ROC, PR curve and calibration below. One of the great things about ML studio is that it automatically tries many different models and shows you the performance of all of them (in this case 75 different models were trained!) The best performing model for this case was a gradient boosting algorithim with a standard scaler wrapper (AUROC = 0.92, accuracy = 0.833). 

![Screenshot 2023-07-01 at 3 51 13 PM](https://github.com/BrunoValan/MLOPS_AutoML/assets/110431113/47e068a6-f5fd-41fc-a7ad-aaae0c96b104)

![Screenshot 2023-07-01 at 3 51 58 PM](https://github.com/BrunoValan/MLOPS_AutoML/assets/110431113/cc36cd96-a140-4705-bcf2-5aaa1cc9fc39)


## Understanding feature impact on outcome
![Screenshot 2023-07-01 at 10 38 22 AM](https://github.com/BrunoValan/MLOPS_AutoML/assets/110431113/d407ec51-3754-415f-b537-b496fa831c6d)

Feature importance is one of the most important things to pay attention to especially in medical machine learning problems where the reason for the outcome is often more important than a high performing model. Here we can see some of the most important health factors to predicting whether or not someone will have heart disease in this data set.



