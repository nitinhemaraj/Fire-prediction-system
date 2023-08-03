# Fire-prediction-system
Fire prediction system is a sophisticated tool designed to forecast and detect potential fire incidents in specific areas. It utilizes various data sources, advanced algorithms, and machine learning techniques to analyze historical and real-time data, enabling early warning and proactive fire management.

It is a project that aims to develop a machine learning model that can predict the confidence level of a potential forest fire based on various attributes and environmental factors. The project employs a dataset containing historical information about forest fire incidents, including attributes such as latitude, longitude, scan, acq_date, acq_time, brightness temperature, satellite type, instrument, and more.

The primary goal of this project is not to predict whether a forest fire will occur or not but to determine the level of confidence in the prediction. This information is crucial for forest management and firefighting authorities to allocate resources and take necessary preventive measures in high-risk areas.

The project follows the following steps:

* Data Collection: The dataset, called "fire_archive.csv," is imported, which contains records of past forest fire incidents along with relevant attributes.

* Data Exploration and Cleaning: The dataset is explored to understand its structure and check for any missing or irrelevant data. Necessary data cleaning and preprocessing techniques are applied to ensure the data's quality and usefulness for model training.

* Feature Engineering: The data is transformed to make it suitable for machine learning models. Categorical variables like "daynight" and "satellite" are converted into numerical form using mapping techniques. The "scan" column is binned to create a categorical variable.

* Data Visualization: Correlation heatmaps are generated to understand the relationships between variables and identify important features that might affect forest fire confidence.

* Model Development: A RandomForestRegressor model is chosen for this prediction task. The dataset is divided into training and testing sets, and the model is trained using the training data.

* Model Tuning: The initial model's performance is evaluated, and hyperparameter tuning is performed using RandomizedSearchCV to find the optimal hyperparameters that improve the model's accuracy and reduce overfitting.

* Model Evaluation: The final tuned model is evaluated using the test dataset to assess its accuracy in predicting the confidence level of forest fires.

* Model Saving: The best-performing model is saved as a pickle file for later use.

Bonus: To optimize the model storage, the pickle file is further compressed using the bz2 module, resulting in a smaller file size without sacrificing model performance.

This project's main outcome is a machine learning model that can accurately predict the confidence level of forest fires based on input attributes. The model can be used by forest departments, firefighting authorities, and environmental agencies to identify high-risk areas, plan preventive measures, and efficiently allocate resources for firefighting efforts. Additionally, the compressed model file ensures that the predictive capability is preserved while reducing the storage requirements.
