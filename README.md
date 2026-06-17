# Feature Store and Feature Engineering Pipeline for Machine Learning

This project demonstrates how to build a simple Feature Store and apply feature engineering inside a Machine Learning pipeline.

The pipeline creates a synthetic dataset, stores the generated features, explores feature distributions and correlations, trains a Random Forest classification model, evaluates its performance, and saves the model artifacts and execution metadata.

## Project Objective

The main objective of this project is to demonstrate the role of a Feature Store in a Machine Learning workflow.

The project shows how to:

* Create a feature store from generated data;
* Organize features and target variables in a structured dataset;
* Explore feature distributions and correlations;
* Train and evaluate a Machine Learning classification model;
* Save model artifacts, predictions, and pipeline execution information;
* Structure a reproducible Machine Learning pipeline.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib

## Project Structure

```text
.
├── pyproject.toml                  # Project configuration and package metadata
├── requirements.txt                # Project dependencies
├── LEIAME.txt                      # Original execution instructions
├── src/
│   ├── projeto5.py                 # Main pipeline script
│   ├── dsa_cria_feature_store.py   # Feature Store creation module
│   ├── dsa_explora_dados.py        # Data exploration and visualization module
│   ├── dsa_treina_modelo.py        # Model training and evaluation module
│   └── dsa_salva_modelo.py         # Model, predictions, and metadata saving module
├── feature_store/
│   └── features.csv                # Generated feature store output
└── pipeline_runs/
    ├── random_forest_dsa.joblib    # Trained model artifact
    ├── previsoes.csv               # Model predictions
    └── pipeline_run_info.json      # Pipeline execution summary
```

## How the Project Works

The pipeline follows these steps:

1. Creates the output folders for the feature store and pipeline runs;
2. Generates a synthetic dataset with informative, derived, and random features;
3. Saves the generated feature set as a CSV file;
4. Performs exploratory analysis with feature distribution plots and a correlation heatmap;
5. Splits the dataset into training and testing sets;
6. Trains a Random Forest classification model;
7. Evaluates the model using accuracy and a classification report;
8. Saves the trained model;
9. Saves predictions with actual and predicted values;
10. Saves pipeline execution information in JSON format.

## Feature Store

The Feature Store is generated from synthetic data and contains:

* Informative features;
* Linear combinations of informative features;
* Random features;
* A binary target variable.

The generated dataset is saved as:

```text
feature_store/features.csv
```

## Model

The project uses a Random Forest classifier:

```text
RandomForestClassifier
```

The model is trained using an 80/20 train-test split and evaluated with:

* Accuracy;
* Classification report;
* Predicted vs. actual values.

## Pipeline Outputs

After running the pipeline, the following files are generated:

```text
feature_store/features.csv
pipeline_runs/random_forest_dsa.joblib
pipeline_runs/previsoes.csv
pipeline_runs/pipeline_run_info.json
```

The `pipeline_run_info.json` file stores metadata such as:

* Model type;
* Model artifact path;
* Feature store path;
* Model accuracy;
* Predictions file path.

## Installation

Create a virtual environment:

```bash
python3 -m venv dsavenv
```

Activate the virtual environment:

```bash
source dsavenv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Install the project in editable mode:

```bash
pip install -e .
```

## Running the Pipeline

Activate the virtual environment:

```bash
source dsavenv/bin/activate
```

Run the main pipeline script:

```bash
python src/projeto5.py
```

After execution, the pipeline will create the feature store, train the model, save the artifacts, and print the execution summary.

## Deactivating the Environment

To deactivate the virtual environment, run:

```bash
deactivate
```

## Notes

* The dataset is generated programmatically for educational purposes.
* The feature store is saved locally as a CSV file.
* The trained model is saved using Joblib.
* The project demonstrates a simplified Machine Learning pipeline focused on feature engineering, feature storage, model training, and artifact tracking.

## Author

Project developed as a practical study on Feature Store construction and feature engineering in Machine Learning pipelines.
