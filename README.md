## 🧠 Handwritten Digit Classifier: Perceptron vs. Naïve Bayes vs. MIRA
**Tech Stack:** Python · Machine Learning · Scikit-learn-style implementation · OCR
---
Please note that this project was completed for CMPT 310: Introduction to AI, taught by Professor Ahmadreza Nezami. He had adapted the course material from Professor Dan Klein and Professor Pieter Abbeel for CS188 Intro to AI at UC Berkeley.
---
Built and compared three supervised machine learning classifiers — **Naïve Bayes**, **Perceptron**, and **MIRA (Margin-Infused Relaxed Algorithm)** — to recognize **handwritten digits (0–9)** using image-based pixel data for an optical character recognition (OCR) task.

- Implemented all classifiers from scratch in Python using vectorized operations and the `Counter` class for feature-weight management.
- **Perceptron:** Trained multi-class perceptron using iterative weight updates based on misclassification; visualized learned weight vectors to analyze feature importance.
- **MIRA:** Extended the perceptron by calculating adaptive update steps (τ) to improve margin and generalization; tuned hyperparameter **C** over a grid search to maximize validation accuracy.
- **Naïve Bayes:** Developed a generative model based on feature likelihoods with Laplace smoothing for unseen features.
- Designed and analyzed performance across classifiers using consistent training, validation, and test sets; performed tuning and model selection.
- Achieved over **75% test accuracy** on digit recognition using minimal features and no external libraries.

## 📁 Project File Overview

Below is a breakdown of the key files I worked with in this project and how each one contributed to building and testing the classifiers:

| **File**                  | **What I Used It For**                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------|
| `naiveBayes.py`           | I implemented the **Naïve Bayes classifier** here. This file contains all the logic for training on image features and predicting digit labels using probabilistic methods. |
| `perceptron.py`           | This is where I wrote the **Perceptron classifier** from scratch, including the multi-class training loop, weight updates, and a method for visualizing the top-weighted features. |
| `mira.py`                 | I implemented the **MIRA (Margin-Infused Relaxed Algorithm)** classifier here. It includes an adaptive margin-based learning algorithm and tuning logic for the hyperparameter `C`. |
| `dataClassifier.py`       | This acted as the **main driver script**. I used it to run my models, test different configurations, extract features, and evaluate performance on validation and test sets. |
| `answers.py`              | This file was used to submit answers to written analysis questions. For example, I explained which visual weight maps were most representative of a Perceptron model. |
| `classificationMethod.py`| Although I didn’t modify this file, I studied it carefully as it defines the **base class for all classifiers** and outlines the method signatures I needed to follow. |
| `samples.py`              | This file helped with **reading and processing image data** from the dataset. It handles formatting the digit images into a feature map suitable for the classifiers. |
| `util.py`                 | A utility file that provided essential tools, such as the `Counter` class, which made working with feature vectors much easier. I relied on this a lot when updating weights. |
| `mostFrequent.py`         | This was a simple **baseline classifier** that always predicts the most common digit. I used it as a reference point to evaluate how well my models performed. |
| `digitdata/`              | This folder contained the actual **handwritten digit image data** (training, validation, and test sets). My classifiers learned from this data to perform OCR tasks. |



> **Outcome:** Gained hands-on experience with foundational ML algorithms and optimization strategies for classification tasks on real-world data.
