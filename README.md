# wafer-fault-detection
* Built a classification methodology to predict the quality of wafer sensors based on the given training data.
* The inputs of various sensors for different wafers have been provided. 
* In electronics, a wafer (also called a slice or substrate) is a thin slice of semiconductor used for the fabrication of integrated circuits.
* The goal was to build a machine learning model which predicts whether a wafer needs to be replaced or not (i.e., whether it is working or not) based on the inputs from various sensors.
* A complete pipelined architecture was used as shown below.
![alt text](architecture.jpg)

├── Data Ingestion  
│   ├── Training_Batch_Files             # Input files for training  
│   ├── Prediction_Batch_files           # Input files for prediction  
│   ├── DataValidation and Insertion     # Validates and inserts data into the database  
│   └── DataTypeValidation_Insertion_Training  # Checks data schema for training  
│  
├── Data Preprocessing  
│   ├── data_preprocessing               # Scripts for preprocessing raw data  
│   └── preprocessing_data               # Intermediate processed data  
│  
├── Model Development  
│   ├── best_model_finder                # Module to select the best ML model  
│   └── models                           # Saved trained models  
│  
├── Model Prediction  
│   ├── predictFromModel.py              # Script to run predictions on new data  
│   ├── Prediction_Output_File           # Outputs of model predictions  
│   ├── Prediction_Database              # Database for prediction data  
│   └── Prediction_Logs                  # Logs for prediction runs  
│  
├── Deployment  
│   ├── main.py                          # Entry point for model deployment  
│   ├── flask_monitoringdashboard.db     # Flask-based dashboard database  
│   └── templates                        # HTML templates for the Flask dashboard  
│  
├── Logs and Reports  
│   ├── Training_Logs                    # Logs for model training  
│   ├── Prediction_Logs                  # Logs for model predictions  
│   └── Report Output                    # Final reports and summaries  
│  
└── Configuration  
    ├── schema_training.json             # Schema definition for training data  
    ├── schema_prediction.json           # Schema definition for prediction data  
    ├── runtime.txt                      # Runtime configuration file  
    └── requirements.txt                 # List of required libraries and dependencies  

