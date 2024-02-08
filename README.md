# Disaster Response Pipeline Project

## Project Overview

In this project, our goal is to develop a model capable of classifying messages sent during disasters into one or more of 36 predefined categories. These categories include Aid Related, Medical Help, Search And Rescue, and others. By accurately classifying these messages, we can ensure they are directed to the appropriate disaster relief agencies, thus facilitating efficient response efforts.

### Approach

Our approach involves building a basic ETL (Extract, Transform, Load) pipeline followed by a Machine Learning pipeline to accomplish the classification task. Here's a breakdown of the key steps:

1. **Data Collection**: We will work with a dataset provided by [Figure Eight](https://www.figure-eight.com/), which contains real messages sent during disaster events.

2. **Data Preprocessing**: This step involves cleaning and preparing the data for model training. We'll handle tasks such as removing duplicates, handling missing values, and tokenizing text.

3. **Feature Engineering**: We'll extract relevant features from the text data that can aid in classification. This might include word embeddings, TF-IDF vectors, or other representations suitable for text data.

4. **Model Building**: Using the preprocessed data and engineered features, we'll train a multi-label classification model. Given the nature of the task, we'll likely explore algorithms like Random Forest, Naive Bayes, or Neural Networks.

5. **Model Evaluation**: We'll evaluate the performance of our model using appropriate metrics for multi-label classification, such as F1-score or Hamming loss. This step will help us understand how well our model generalizes to unseen data.

6. **Web Application**: Finally, we'll deploy the trained model into a web application where users can input a message and receive classification results in real-time.

### Project Components

- **ETL Pipeline**: Responsible for extracting data from the source, transforming it into a suitable format, and loading it for further processing.
  
- **Machine Learning Pipeline**: This pipeline involves steps like data preprocessing, feature engineering, model training, and model evaluation.

- **Web Application**: A user-friendly interface allowing users to input messages and receive classification results using the trained model.

### Technologies Used

- Python: For data preprocessing, model building, and web application development.
- Libraries like Pandas, Scikit-learn, and NLTK for data manipulation, machine learning, and natural language processing tasks.
- Flask: A lightweight web framework for developing the web application.
- HTML/CSS/JavaScript: For designing and implementing the user interface of the web application.

By the end of this project, we aim to deliver an efficient and reliable system for classifying disaster-related messages, thereby aiding in effective disaster response efforts.

![Screenshot of Web App](WebApp.PNG)

## File Description
~~~~~~~
        disaster_response_pipeline
          |-- app
                |-- templates
                        |-- go.html
                        |-- master.html
                |-- run.py
          |-- data
                |-- disaster_message.csv
                |-- disaster_categories.csv
                |-- DisasterResponse.db
                |-- process_data.py
          |-- models
                |-- classifier.pkl
                |-- train_classifier.py
          |-- Preparation
                |-- categories.csv
                |-- ETL Pipeline Preparation.ipynb
                |-- ETL_Preparation.db
                |-- messages.csv
                |-- ML Pipeline Preparation.ipynb
                |-- README
          |-- README
~~~~~~~
## Installation
Must runing with Python 3 with libraries of numpy, pandas, sqlalchemy, re, NLTK, pickle, Sklearn, plotly and flask libraries.

## File Descriptions
1. App folder including the templates folder and "run.py" for the web application
2. Data folder containing "DisasterResponse.db", "disaster_categories.csv", "disaster_messages.csv" and "process_data.py" for data cleaning and transfering.
3. Models folder including "classifier.pkl" and "train_classifier.py" for the Machine Learning model.
4. README file
5. Preparation folder containing 6 different files, which were used for the project building. (Please note: this folder is not necessary for this project to run.)

## Instructions
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

## Licensing, Authors, Acknowledgements
Many thanks to Figure-8 for making this available to Udacity for training purposes. Special thanks to udacity for the training. Feel free to utilize the contents of this while citing me, udacity, and/or figure-8 accordingly.

### NOTICE: Preparation folder is not necessary for this project to run.
