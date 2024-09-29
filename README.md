
# Rental Bikes on Demand: Predictive Analytics for Hourly Bike Rental Demands
#### - Dataset Details: 
- Rental bikes are extremely popular in South Korea, offering easy access and a safe way to commute over medium distances. In Seoul, bike rental spots are everywhere, providing locals with convenient access to bicycles. Ensuring their availability and accessibility year-round is crucial for maintaining a reliable commuting option and enhancing the stability of urban transportation.
- The dataset includes weather-related features, temperature, humidity, wind speed, visibility, dew point, solar radiation, snowfall, and rainfall. It also provides information on the number of bikes rented per hour and corresponding date details.
- The dataset has 8,760 observations and 14 features.
- Missing values have been removed from the dataset.

# Dataset
#### - Name: Seoul Bike Sharing Demand
#### - Dataset Source: https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand

- ## Phase 1 Summary
    Phase 1 consists of three key stages for implementing machine learning for a business. It involves understanding the business, the data, and preparing the data for machine learning models. Understanding the business' project objectives and requirements from a business point of view helps guide the project with the goal of predicting hourly bike rental demands in Seoul, South Korea, ensuring optimal availability and service reliability. With the given dataset, I had to familiarize myself with it by researching its source and its intended purpose by exploring the dataset to understand its structure, content, and quality. Assessing data quality and identifying any issues, such as missing values or anomalies, is also a part of this stage. For the data preparation stage, I needed to keep in mind what the business' goal was and prepare the data fit for predicting hourly bike rentals. This involved splitting the date into components like days, months, years, days of the week, and weekends to create meaningful features for the model. Making sure each feature is correctly assigned the appropriate data type, analyzing the relationships between different weather features and understanding how they can be used in machine learning is also necessary. Ensuring each feature is useful for machine learning, such as identifying and removing functioning days feature, is part of this process. Finally, visualizing each feature helps extract insights and understand its distribution and relationships with other features.

    Phase 2 consists of modelling and evaluations. Without understanding the business, we would not have a framework as to what the goal is. Understanding the data helps us know which model to implement and the evaluations needed and preparing the data for modelling creates a framework for us to build on in phase 2. This framework guides us in selecting the appropriate machine learning models. For instance, using a logistic regression model to predict bike rentals wouldn't make sense if all the data in the dataset is not categorical. Therefore, if we want to use a logistic regression model, we need to prepare the dataset correctly first.

    - ## Report Overview

    ### Context and Aim

    This report focuses on predicting hourly bike rental demands in Seoul, South Korea. The aim is to develop and evaluate various machine learning models to ensure optimal availability and service reliability of rental bikes. The report builds on the initial data exploration and preparation conducted in Phase 1, progressing to model fitting, hyperparameter tuning, and performance evaluation in Phase 2.
    Main Findings

    - Poisson Regressor: The Poisson Regressor was well-suited for count data, providing reasonable predictions with a mean Poisson deviance of 226. This model was further stabilized using bootstrap sampling.

    - Ensemble Model: Combining models with and without feature selection resulted in an improved performance over the individual models, demonstrating the benefit of ensemble methods.

    - Histogram-based Gradient Boosting Regressor: This model showed the best performance with a mean Poisson deviance of 37.20, an R² score of 0.92, indicating a high level of accuracy and efficiency.

    - XGBoost: While effective, XGBoost did not perform as well as the Gradient Boosting Regressor, with a mean Poisson deviance of 150.85 and an R² score of 0.79.
        
    - Neural Network: The neural network model, though basic, achieved a mean Poisson deviance of 156.98, demonstrating potential for future improvements with more advanced architectures and tuning.

    ### Key Takeaway

    The Histogram-based Gradient Boosting Regressor emerged as the most effective model for predicting hourly bike rental demands, providing high accuracy and efficiency. Ensemble methods and neural networks also showed promise, indicating potential for further exploration and refinement.

    ### Recommendations

    - Adopt Gradient Boosting: Implement the Histogram-based Gradient Boosting Regressor for predicting bike rental demands due to its superior performance.
        
    - Explore Advanced Tuning: Consider using advanced hyperparameter tuning techniques such as Bayesian optimization to further improve model performance.
    
    - Incorporate Additional Features: Enhance the model by integrating additional relevant features such as the air quality index (AQI) and heat index to capture environmental influences on bike rental patterns.

    - Advanced Neural Network Architectures: Invest in developing more sophisticated neural network models with varied architectures and regularization techniques to potentially achieve even better accuracy.

    - Efficiency Improvements: Explore more efficient methods like random search or alternative ensemble techniques to reduce computational costs while maintaining high model performance.