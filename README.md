
# 🚴‍♂️ Bike Sharing Demand Prediction with AutoGluon

## 📖 Overview

This project aims to predict bike-sharing demand using AutoGluon, a powerful AutoML library. The process involves setting up Kaggle API access, downloading the dataset, preprocessing the data, and building predictive models. The project includes steps for data exploration, feature engineering, model training, hyperparameter optimization, and submission to the Kaggle competition.

## 📂 Project Structure

The project directory is organized as follows:

```
Predict_Bike_Sharing_Demand_Udacity_project1/
│
├── Data/
│   ├── train.csv
│   ├── test.csv
│   └── sampleSubmission.csv
│
├── Bike_Sharing_Demand.ipynb
├── Bike_Sharing_Demand.py
├── README.md
├── report-template.md
├── requirements.txt
├── kaggle_scores.png
├── top_model_performance.png
└── Bike_Sharing_Demand.html
```

- **📁 Data/**: Contains the datasets for training, testing, and submission.
- **📓 Bike_Sharing_Demand.ipynb**: Jupyter notebook with the main code for data processing, model training, and evaluation.
- **📜 Bike_Sharing_Demand.py**: Python script for executing the bike demand prediction.
- **📝 README.md**: This file, detailing the project overview, setup instructions, and usage.
- **🗂️ report-template.md**: Markdown template for the project report.
- **📊 kaggle_scores.png**: Plot showing Kaggle competition scores.
- **📈 top_model_performance.png**: Plot showing the performance of the top model.
- **🌐 Bike_Sharing_Demand.html**: Exported HTML version of the Jupyter notebook.

## ⚙️ Setup Instructions

### 🛠️ Requirements

Ensure Python 3.x is installed and the necessary libraries are listed in `requirements.txt`.

### 🏗️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Ganesh2409/Predict_Bike_Sharing_Demand.git
   cd Predict_Bike_Sharing_Demand
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## 📝 Project Details

### Step 1: Kaggle Account Setup

- **👤 Create a Kaggle Account**: Register on Kaggle and obtain an API key.
- **🔑 Setup Kaggle API Key**: Save the API key in the `.kaggle` directory.

### Step 2: Download the Dataset

- **📥 Download**: Use the Kaggle API to download and unzip the dataset.

### Step 3: Data Loading and Exploration

- **📊 Load Data**: Import datasets (`train.csv`, `test.csv`, `sampleSubmission.csv`) and parse datetime columns.
- **🔍 Explore Data**: Examine data statistics and initial summaries.

### Step 4: Train a Model with AutoGluon

- **🔧 Preprocessing**: Drop irrelevant columns (`casual`, `registered`) and set the `count` column as the target.
- **🤖 Model Training**: Use AutoGluon’s `TabularPredictor` with a 10-minute time limit and `best_quality` preset.
- **📈 Evaluation**: Review model performance and generate predictions for the test set.

### Step 5: Feature Engineering

- **🛠️ Add Features**: Extract and add new features such as year, month, day, and hour from the `datetime` column.
- **🔤 Categorical Encoding**: Convert categorical features (`season`, `weather`) to category type.

### Step 6: Rerun the Model

- **🔄 Update Features**: Re-train the model with the new features and evaluate performance.
- **📤 Submission**: Prepare and submit the updated predictions to Kaggle.

### Step 7: Hyperparameter Optimization

- **🔬 Tune Hyperparameters**: Optimize model hyperparameters for better performance.
- **📊 Final Evaluation**: Generate predictions and submit to Kaggle, and review the results.

### 🎯 Results

- **🏁 Initial Score**: 1.80367
- **🚀 Score with Additional Features**: 0.51204
- **🎯 Score with Hyperparameter Optimization**: 0.54099

### 📊 Report

- **📈 Visualization**: Includes plots of model scores and hyperparameter impacts.
- **🗒️ Hyperparameter Table**: Summary of hyperparameters and corresponding scores.

### 🚀 Running the Code

To execute the bike demand prediction script:

```bash
python Bike_Sharing_Demand.py
```

To open and run the Jupyter notebook:

```bash
jupyter notebook Bike_Sharing_Demand.ipynb
```

## 🔚 Conclusion

This project utilizes AutoGluon for predicting bike-sharing demand and showcases the end-to-end process from data acquisition to model submission. By leveraging AutoML, the project demonstrates a robust approach to predictive modelling in a Kaggle competition.

```bash
Made with ❤️ ( ͡• ͜ʖ ͡• ) Follow for more  ... :)
