# Fake News Detection using Machine Learning

This repository contains a machine learning project developed as part of the course **"Apprentissage et Reconnaissance de Formes"**. The goal of the project is to apply the machine learning techniques studied during the course to a real-world classification problem: **detecting fake news from textual data**.

The project implements several classical machine learning models to classify news articles as **real or fake** based on their textual content.

---

## Dataset

The dataset used in this project is the **LIAR2 dataset**, which is publicly available online: https://github.com/chengxuphd/liar2

Each entry in the dataset contains several attributes, including:

- **statement** – the textual claim or statement
- **speaker** – the person who made the statement
- **context** – the context in which the statement was made
- **label** – the truthfulness label assigned to the statement

The dataset includes several truthfulness categories such as:

- `true`
- `mostly-true`
- `half-true`
- `barely-true`
- `false`
- `pants-fire`

For the purposes of this project, these labels are used to train machine learning models capable of distinguishing between **reliable and unreliable statements**.

The dataset is organized into three main files:

- `train.tsv` – training dataset
- `valid.tsv` – validation dataset
- `test.tsv` – testing dataset

These files allow us to train and evaluate the models in a structured way.

---

## Methodology

The project follows a classical **machine learning pipeline for text classification**.

### 1. Data Preprocessing

The textual data is first cleaned and prepared for machine learning models. This includes:

- Removing punctuation and unnecessary symbols  
- Converting text to lowercase  
- Tokenization and normalization  
- Transforming text into numerical features  

To convert text into numerical vectors, we use **TF-IDF (Term Frequency – Inverse Document Frequency)** representation.

---

### 2. Machine Learning Models

Several supervised learning algorithms were implemented and compared:

- **Logistic Regression**
- **Naive Bayes**
- **Support Vector Machines (SVM)**

These algorithms are commonly used for **text classification problems** due to their efficiency and strong performance on high-dimensional sparse data such as TF-IDF vectors.

---

### 3. Training and Evaluation

The dataset is split into **training and testing sets** in order to evaluate the performance of the models.

The models are evaluated using standard classification metrics:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**

These metrics allow us to measure how effectively the model distinguishes between real and fake news articles.

---

## Results

The implemented models achieved strong performance in detecting fake news.

In general:

- **Logistic Regression and SVM** provided the best performance.
- **Naive Bayes** performed slightly worse but remained computationally efficient.

The results show that classical machine learning approaches combined with **TF-IDF text representation** can effectively detect fake news patterns in textual data.

---
