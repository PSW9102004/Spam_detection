# Spam Detection

A simple SMS spam detection project using machine learning, built with Python.

## Table of Contents

* [Introduction](#introduction)
* [Features](#features)
* [Dataset](#dataset)
* [Requirements](#requirements)
* [Installation](#installation)
* [Usage](#usage)
* [Project Structure](#project-structure)
* [Model Training](#model-training)
* [Running the App](#running-the-app)
* [Results](#results)
* [License](#license)

## Introduction

This project demonstrates a basic end-to-end pipeline for SMS spam detection:

1. Loading and exploring the dataset (`spam.csv`).
2. Text preprocessing and feature extraction using a vectorizer.
3. Training a machine learning model to classify messages as "spam" or "ham".
4. Saving the trained model and vectorizer.
5. Building a web app (`app.py`) to provide an interactive interface for real-time predictions.

## Features

* Exploratory Data Analysis (EDA).
* Text cleaning and preprocessing.
* Vectorization of text inputs.
* Model training and evaluation.
* Serialization of model and vectorizer objects.
* Simple web interface for live predictions.

## Dataset

The dataset used is a collection of SMS messages labeled as spam or ham (non-spam). It is provided in `spam.csv` with the following columns:

| Column  | Description                                 |
| ------- | ------------------------------------------- |
| `label` | Indicates if the message is `spam` or `ham` |
| `text`  | The raw SMS message content.                |

## Requirements

* Python 3.7+
* Packages listed in `requirements.txt`:

  * `pandas`
  * `scikit-learn`
  * `flask` (or `streamlit` if used)
  * (etc.)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/PSW9102004/Spam_detection.git
   cd Spam_detection
   ```
2. (Optional) Create and activate a virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Model Training and Evaluation

In `sms-spam-detection.ipynb`, you will find code for:

1. Loading `spam.csv`.
2. Preprocessing text (lowercasing, removing punctuation, stopwords, etc.).
3. Splitting data into training and test sets.
4. Vectorizing text using `TfidfVectorizer` (or other).
5. Training a classifier (e.g., `MultinomialNB`, `LogisticRegression`).
6. Evaluating model performance (accuracy, precision, recall, F1-score).
7. Saving the trained model (`model.pkl`) and vectorizer (`vectorizer.pkl`).

To run the notebook:

```bash
jupyter notebook sms-spam-detection.ipynb
```

### Running the Web App

The web application provides a simple interface to test messages in real time.

```bash
python app.py
```

1. Open your browser at `http://localhost:5000` (or the port indicated).
2. Enter an SMS message.
3. Click **Predict** to see if it's spam or ham.

## Project Structure

```
Spam_detection/
├── README.md
├── spam.csv
├── sms-spam-detection.ipynb
├── app.py
├── model.pkl
├── vectorizer.pkl
└── requirements.txt
```

* **spam.csv**: Raw SMS dataset.
* **sms-spam-detection.ipynb**: Notebook for data analysis and model training.
* **app.py**: Web application script for live predictions.
* **model.pkl**: Serialized trained model.
* **vectorizer.pkl**: Serialized text vectorizer.

## Model Training

If you wish to retrain the model on new data or tweak parameters:

1. Open the notebook.
2. Adjust the preprocessing steps or classifier parameters.
3. Re-run all cells.
4. Save the new `model.pkl` and `vectorizer.pkl`.

## Running Tests



## Results

Include sample performance metrics:

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 0.98  |
| Precision | 0.95  |
| Recall    | 0.93  |
| F1-Score  | 0.94  |




---

*Happy coding!*


