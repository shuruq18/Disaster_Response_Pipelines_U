# Disaster_Response_Pipelines_U
[Figure Eight](https://www.figure-eight.com/) has provided data related to messages, categorized into different classifications, that have been received during emergencies/disasters.
This project try to recognize these categories in order to cater for quicker responses to the emergency messages.
Using machine learning techniques, (Random Forest Classifier) we shold be able to predict the category.

### The process was carried out as follows:

1. Data Processing
    Assessing and cleaning the data, so that it can be utilized by machine learning algorithms.
    See details in the [ETL Notebook]
    
2. Model training
    Data was passed through a pipeline and a prediction model is made.
    See details in the [ML Notebook]

3. Prediction and Visualization
    Making a [web app](https://view6914b2f4-3001.udacity-student-workspaces.com/) for prediction and visualization, where user may try some emergency messages and see visualization of distribution of genres and categories.
        
### Instructions:
#### Run the following commands in the project's root directory to set up database and model:

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

#### Run the following command in the app's directory to run your web app:

`python run.py`

#### Go to http://0.0.0.0:3001/
 
### File structure of project:

1.  ../app - folder for web app

    ../app/run.py - flask web app
    
    ../templates - .html templates
    

2.  ../data - folder for files for the datasets

    ../data/disaster_categories.csv - raw file containing the categories
    
    ../data/disaster_messages.csv - raw file containing the messages
    
    ../data/process_data.py
    
    ../data/disaster_response.db - database created when running `python process_data.py`
    
    ../data/DisasterResponse.db - database for the clean data
    

3.  ../models - folder for the classifier model and pickle file

    ../models/train_classifier.py - model training script
    
    ../models/classifier.pkl - saved model when running `python train_classifier.py`
    

4.  README.md
