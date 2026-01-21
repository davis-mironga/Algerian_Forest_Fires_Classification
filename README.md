# Algerian Forest Fires Classification

## Project Overview
This project aims to predict forest fires in Algeria based on various weather-related features such as temperature, humidity, wind speed, and more. The dataset is sourced from two regions in Algeria: Bejaia and Sidi-Bel Abbes. The project involves data cleaning, exploratory data analysis (EDA), building machine learning models, and evaluating their performance.

## Folder Structure
Here is the directory structure of the project:


Algerian_Forest_Fires_Classification/
│
├── data/ # Contains the raw and processed datasets
├── src/ # Source code folder
│ ├── functions/ # Utility functions (e.g., visualizations, utilities)
│ ├── data_preprocessing/ # Data cleaning and preprocessing scripts
│ ├── evaluation/ # Model evaluation scripts
│ └── model/ # Model training, hyperparameter tuning, and saving scripts
├── notebooks/ # Jupyter notebooks for data cleaning, EDA, and modeling
├── models/ # Saved models
├── requirements.txt # Python dependencies
├── README.md # Project description
└── .gitignore # Git ignore file


## Setup Instructions

### Clone the Repository
To get started with this project, clone the repository using Git:

```bash
git clone <your-repository-url>
cd Algerian_Forest_Fires_Classification

Install Dependencies

This project requires several Python libraries. You can install all dependencies by using the following command:

pip install -r requirements.txt


Project Workflow
1. Data Preprocessing:

The first step in this project was to clean and preprocess the data. We loaded the dataset from Excel files, handled missing values, encoded categorical features, and performed feature engineering.

The data preprocessing steps are contained in the src/data_preprocessing/ folder. Scripts like data_cleaning.py and feature_engineering.py are used to handle the data preparation tasks.

2. Exploratory Data Analysis (EDA):

In this step, we analyzed the dataset visually and statistically to understand the distributions and correlations between features. The EDA is performed in the 02_eda.ipynb notebook, where we also used visualizations to better understand the dataset.

3. Modeling:

After preprocessing and performing EDA, we moved on to modeling. We trained machine learning models such as Logistic Regression and Random Forest.

The modeling process can be found in the 03_modeling.ipynb notebook, which includes:

Data splitting into training and testing sets.

Model training and evaluation using metrics like accuracy, precision, recall, F1-score, and AUC-ROC.

The models are saved in the models/ folder using joblib to allow for easy reloading and prediction.

4. Model Saving and Loading:

Once the models were trained, they were saved in the models/ folder as .pkl files. These models can be loaded at any point for further use or prediction without retraining.


5. Model Evaluation:

After saving and loading the models, they were evaluated on the test data. Evaluation metrics such as accuracy, precision, recall, F1-score, and AUC-ROC were calculated to compare model performance.

The model evaluation scripts can be found in the src/evaluation/ folder.


How to Use the Code

Train a model:

Run train_model.py in the src/model/ folder to train the model.

Evaluate the model:

Use model_evaluation.py in the src/evaluation/ folder to evaluate the model's performance.

Save the trained models:

Once models are trained, you can save them using the save_model.py script in the src/model/ folder.

Load and use saved models:

The saved models can be loaded and used for prediction without retraining by using the provided joblib.load() method.


Folder Details

data/: Contains raw and processed datasets.

src/: Contains all the source code for the project.

functions/: Helper functions used throughout the project (e.g., for plotting or custom transformations).

data_preprocessing/: Code for cleaning and preprocessing the dataset.

evaluation/: Code for evaluating model performance.

model/: Code for training, saving, and tuning machine learning models.

models/: This folder contains the saved trained models (log_reg_model.pkl, random_forest_model.pkl).

notebooks/: Jupyter notebooks for each stage of the project (data cleaning, EDA, modeling).

requirements.txt: Contains the required Python dependencies.

.gitignore: Specifies files and folders that should not be tracked by Git (e.g., model files, data files, and virtual environments).

License

This project is licensed under the MIT License - see the LICENSE
 file for details.