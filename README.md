# Pneumonia Detection with AutoML (Udacity AI Product Management Nanodegree)

This project demonstrates a machine learning solution designed to help doctors quickly identify cases of pneumonia in children using chest X-ray images. Leveraging AWS Rekognition (AutoML), I built, evaluated, and iterated on several classification models, focusing on how data quality, balance, and labeling impact model performance.

> ✅ October 21, 2024

---

## Project Overview

The goal of this project was to:

- Build binary and multi-class classification models using AutoML
- Understand the impact of balanced vs. unbalanced data
- Explore the effects of mislabeled (dirty) data
- Experiment with increasing data volume to improve performance

The models were trained using the Kaggle Chest X-ray dataset, which contains pediatric chest X-ray images labeled as normal or pneumonia (further divided into bacterial or viral pneumonia).

---

## Project Structure

### 1. Binary Classifier (Balanced Data)
- 100 normal images + 100 pneumonia images
- Evaluated:
  - Train/test split
  - Confusion matrix
  - Precision and recall

![alt text](<Balanced Clean Model.jpg>)

### 2. Binary Classifier (Unbalanced Data)
- 100 normal images + 200 pneumonia images
- Evaluated:
  - How unbalanced classes affect:
    - Confusion matrix
    - Precision and recall
    - Overall model behavior

![alt text](<Unbalanced Clean Model.jpg>)

### 3. Binary Classifier (Dirty Data)
- 100 normal + 100 pneumonia images, with 30% of labels flipped
- Evaluated:
  - Impact on confusion matrix
  - Impact on precision and recall
  - Sensitivity to mislabeled data

![alt text](<Balanced Dirty Model.jpg>)

### 4. Three-Class Model
- 100 normal + 100 bacterial pneumonia + 100 viral pneumonia images
- Evaluated:
  - Multi-class confusion matrix
  - Precision and recall across three classes
  - How much additional data is needed to achieve at least 85% precision and recall

![alt text](<3 Class Balanced Clean Model.jpg>)

---

## Tools and Technologies

- AWS Rekognition AutoML (for model training, hosting, and evaluation)
- Kaggle Chest X-ray dataset

---

## Results and Insights

- Balanced data provided reliable precision and recall but required careful configuration.
- Unbalanced data led to biased predictions, skewing performance metrics.
- Dirty (mislabeled) data significantly degraded performance, highlighting the importance of clean datasets.
- Adding more data improved performance, especially when class balance was maintained.

---

## Key Takeaways

- AutoML platforms like AWS Rekognition can accelerate machine learning product development without extensive manual model coding.
- Data balance and label quality are critical to achieving fair and accurate predictions.
- Iterative experimentation is essential to align product goals (such as clinical reliability) with model performance.