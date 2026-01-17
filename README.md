# IMDB Movie Review Sentiment Analysis

Built from scratch as part of my AI/ML internship preparation.

##  Project Overview
Sentiment analysis system that classifies movie reviews as positive or negative with **89.35% accuracy** using custom Bag of Words implementation and Logistic Regression.

##  Tech Stack
- **Languages:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Scipy, Regex
- **Techniques:** NLP, Text Preprocessing, Bag of Words, Sparse Matrices

##  Key Features
- Custom text preprocessing pipeline (HTML removal, lowercasing, punctuation handling)
- Manual Bag of Words implementation using sparse matrices (99,420 features)
- Logistic Regression classifier
- Proper train/test split (80/20) with stratification

##  What I Learned
- Text preprocessing for NLP tasks
- Memory efficiency with sparse matrices (5B cells → 500MB)
- Trade-offs between model complexity and interpretability
- Importance of proper evaluation (avoiding overfitting)

##  Results
```
Test Accuracy: 89.35%
Precision: 90% (Negative), 89% (Positive)
Recall: 89% (Negative), 90% (Positive)
F1-Score: 89% (Both classes)
```
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/0d3c97fd-69da-4099-b670-84c08a102feb" />


##  Future Improvements
- Implement TF-IDF weighting
- Add n-grams for better context
- Try advanced models (SVM, LSTM)
- Build web interface with Streamlit

##  Project Structure
```
├── sentiment_analysis.ipynb    # Main notebook
├── README.md                   # This file
└── requirements.txt            # Dependencies
```

##  How to Run
```bash
pip install -r requirements.txt
jupyter notebook sentiment_analysis.ipynb
```
