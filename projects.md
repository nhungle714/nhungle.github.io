---
layout: page
title: ML Projects
subtitle: Data Science is Fun
---

## Experience
+ **NBCUniversal**: 

    + **Sentiment Analysis** Developed a sentiment analysis model using Nielsen Social's Twitter data. The fine-tuned BERT model achieved 80% out-of-sample accuracy and will be deployed to develop the sentiment analysis metric to evaluate social impacts of nominee suggestions for People's Choice Award. 
    
    + **Program View Forecasting** Developed a linear regression model to forecast the number of views for NBCUniversal's shows. This model performed equally well with a complicated ARIMA model currently in place.

+ **RubiconMD**: Fully responsible for the development and deployment of a Logistic Regression model to predict medical specialty based on the medical context provided by primary care doctors. The model achieved average out-of-sample AUC score of 0.94 for the top 10 most popular specialties. After the deployment using AWS and Airflow, the model reduces primary care providers' waiting time for  specialist's responses by 25%.


## Projects
+ **[Breast Cancer Classification](https://github.com/nhungle714/Breast_Cancer_Classification)**: Classified benign vs. malignant breast tumors from mammograms, using transfer learning and deep learning with residual connections. Model achieved average out-of-sample AUC score of 0.85.

+ **[Breast Cancer Classification - CSV Data](https://github.com/nhungle714/Data_Science_Projects/tree/master/BreastCancer_CSV)**: Classified benign vs. malignant breast tumors, however, from collected features in the CSV format. Applying Multi-perceptron model instead of Logistic Regression improved out-of-sample AUC score from 0.73 to 0.82.

+ **[ICU Survival](https://github.com/nhungle714/Data_Science_Projects/tree/master/ICU_Survival)**: Predicted ICU survival rate given information recorded at the point patients were admitted to ICUs. This project dealt with missing data and tried applying a simple Multi-Perceptron model (MLP) and a 1D convolutional neural net (CNN) model. The MLP with out-of-sample AUC of 0.89 outperformed the CNN model with out-of-sample AUC of 0.84. This proved that for medical record of missing data and relatively low volume (~91,000 samples), complicated deep learning models do not necessarily perform well.

+ **[Music Recommender System with Implicit Feedback]**: Used Spark's Alternating Least Squares (ALS) method to learn latent factor representations for users and items and tuned the dimension of the latent factors, the regularization parameter, and the scaling parameters. The recommender system on 6 million data points achieved Mean Average Precision (MAP) score of 0.039.

+ **[Avocado Price Forecasting](https://github.com/nhungle714/Data-Science-Projects/tree/master/Avocado_Prices)**: Forecasted avocado prices in different regions given historical average avocado prices by region and by type (i.e., conventional vs. organic), using Prophet.

+ **[House Price Prediction](https://github.com/nhungle714/Data_Science_Projects/tree/master/House_Prices)**: Predicted housing price with Root Meant Square Error RMSE score of 0.1407. This project demonstrated exploratory data analysis to engineer features and investigate distribution of housing prices. Modeling methods of Linear Regression and XGBoost with Lasso regularization, and hyper-parameter tuning boosted model performance while overcoming overfiting.