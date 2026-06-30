# README.md

# Iris Classification with Vertex AI Custom Container

## Project Overview

This project demonstrates how to train, save, and deploy an **Iris flower classification model** using **Google Cloud Vertex AI** with a **custom prediction container**. The repository contains the training data, model training script, and a Jupyter notebook that explains the complete deployment workflow.

---

## Project Structure

```
.
├── data_v1.csv
├── data_v2.csv
├── main.py
├── SDK_Custom_Container_Prediction.ipynb
└── README.md
```

---

## File Descriptions

### `data_v1.csv`

- Primary Iris dataset used for model training.
- Contains flower measurements:
  - Sepal Length
  - Sepal Width
  - Petal Length
  - Petal Width
- Includes the target column `species`.
- Used by `main.py` to train the Decision Tree classifier.

---

### `data_v2.csv`

- Second version of the Iris dataset.
- Can be used for testing, validation, or comparing predictions against another dataset.
- Maintains the same feature structure as the training dataset.

---

### `main.py`

Python script responsible for the complete model training workflow.

Main functionalities include:

- Loading the dataset
- Splitting data into training and testing sets
- Training a Decision Tree Classifier
- Evaluating model accuracy
- Saving the trained model as `model.pkl`

Libraries used:

- pandas
- numpy
- scikit-learn
- pickle

Output:

- Prints model accuracy
- Generates `model.pkl` for deployment

---

### `SDK_Custom_Container_Prediction.ipynb`

A Jupyter Notebook demonstrating how to deploy the trained machine learning model on **Google Cloud Vertex AI** using a **custom container**.

The notebook covers:

- Installing Vertex AI SDK
- Preparing the Iris dataset
- Training and exporting the model
- Building a custom prediction service using FastAPI
- Creating a Docker image
- Uploading the container to Artifact Registry
- Deploying the model to Vertex AI
- Sending online prediction requests
- Testing deployed endpoints

This notebook serves as the deployment guide for the project.

---

## Workflow

1. Prepare the dataset.
2. Train the Decision Tree model using `main.py`.
3. Save the trained model as `model.pkl`.
4. Build a custom prediction container.
5. Push the container image to Google Artifact Registry.
6. Deploy the model on Vertex AI.
7. Send prediction requests to the deployed endpoint.

---

## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- pickle
- Google Cloud Vertex AI SDK
- Docker
- Google Cloud Platform account

Install required packages:

```bash
pip install pandas numpy scikit-learn google-cloud-aiplatform
```

---

## Expected Output

Running `main.py` will:

- Train a Decision Tree classifier
- Display classification accuracy
- Save the trained model as:

```
model.pkl
```

The notebook can then be used to deploy this model as a scalable prediction service on Vertex AI.

---

## Technologies Used

- Python
- Scikit-learn
- Decision Tree Classifier
- Google Cloud Vertex AI
- FastAPI
- Docker
- Jupyter Notebook

---

## Purpose

This project demonstrates an end-to-end machine learning deployment pipeline, from model training to cloud-based online prediction using Google Cloud Vertex AI custom containers.
