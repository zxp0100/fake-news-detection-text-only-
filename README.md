# I have created a GitHub repository for my project, Fake News Detection (Text Only - Binary Classification: True or False). The project focuses on classifying news as either true or false using machine learning and deep learning models.

Datasets Used:
LIAR ([Link](https://sites.cs.ucsb.edu/~william/data/))
Fake News Database ([Link](https://zenodo.org/records/10354245))

Feature Extraction:
1) TF-IDF (Term Frequency-Inverse Document Frequency)
2) Sentiment Score (Using VADER)

Models Implemented:
1) Traditional Machine Learning Models:
Random Forest (RF),
Passive Aggressive Classifier (PAC),
Support Vector Machine (SVM),
Logistic Regression (LR),
Naïve Bayes (NB)

2) Deep Learning Model:
Bidirectional LSTM (Bi-LSTM)

Approach:
1) Training and evaluating individual models using TF-IDF with and without sentiment scores.
2) Implementing ensemble models using hard voting and soft voting to combine multiple classifiers.
