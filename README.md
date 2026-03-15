# Fake News Detection using Machine Learning and Deep Learning

This repository contains a project developed as part of the course **"Machine Learning" / "Apprentissage et Reconnaissance de Formes"**. The goal of the project is to apply the machine learning techniques studied during the course to a real-world classification problem: **detecting fake news from textual data**.

The project implements both **classical machine learning models** and a **deep learning model** to classify statements as **real or fake** based on their textual content.

**Authors:**
- **Raul Fonseca Poça**
- **Juan Diego Zuñiga Vargas**

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

For the purposes of this project, these labels are used to train models capable of distinguishing between **reliable and unreliable statements**.

The dataset is organized into three main files:

- `train.csv` – training dataset
- `valid.csv` – validation dataset
- `test.csv` – testing dataset

These files allow us to train, tune, and evaluate the models in a structured way.

---

## Methodology

The project follows both a **classical machine learning pipeline** and a **deep learning approach for text classification**.

### 1. Data Preprocessing

The textual data is first cleaned and prepared for the models. This includes:

- Removing unnecessary symbols
- Converting text to lowercase when appropriate
- Organizing textual attributes into structured inputs
- Transforming text into numerical features

For the classical models, text is converted into numerical vectors using **TF-IDF (Term Frequency – Inverse Document Frequency)** representation.

For the deep learning model, the text is formatted into a structured input and then tokenized before being processed by the neural network.

---

### 2. Classical Machine Learning Models

Several supervised learning algorithms were implemented and compared:

- **Logistic Regression**
- **Naive Bayes**
- **Support Vector Machines (SVM)**

These algorithms are commonly used for **text classification problems** due to their efficiency and strong performance on high-dimensional sparse data such as TF-IDF vectors.

---

### 3. Deep Learning Model

In addition to the classical models, the project also implements a **transformer-based deep learning model**:

- **DistilBERT**

DistilBERT is a lighter version of BERT based on the transformer architecture. It is pretrained on large-scale text corpora and then fine-tuned for the fake news detection task. Unlike the classical models, it does not rely on TF-IDF features, but instead learns contextual representations directly from tokenized text.

---

### 4. Training and Evaluation

The dataset is divided into **training**, **validation**, and **testing** sets.

- The **training set** is used to learn the model parameters.
- The **validation set** is used to compare configurations and tune hyperparameters.
- The **test set** is used for the final evaluation.

The models are evaluated using standard classification metrics:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**

These metrics allow us to measure how effectively each model distinguishes between real and fake statements.

---

## Results

The implemented models achieved strong performance in detecting fake news.

In general:

- **DistilBERT** provided the best overall performance.
- **Logistic Regression and SVM** also achieved strong results among the classical models.
- **Naive Bayes** performed slightly worse but remained computationally efficient.

The results show that classical machine learning approaches combined with **TF-IDF text representation** are effective baselines, while the **deep learning transformer model** was better able to capture contextual and semantic information from the statements, leading to the highest predictive performance.

---