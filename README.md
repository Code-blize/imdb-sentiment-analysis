# IMDB Movie Review Sentiment Analysis

Built from scratch as part of my AI/ML internship preparation - demonstrates end-to-end NLP pipeline implementation.

##  Project Overview
Sentiment analysis system that classifies IMDB movie reviews as positive or negative with **89.35% accuracy**. Built entirely from scratch using custom Bag of Words implementation and Logistic Regression, without relying on high-level NLP libraries.

##  Dataset
- **Source:** [IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)
- **Size:** 50,000 reviews (25,000 positive, 25,000 negative)
- **Features:** Review text, Sentiment label
- **Balance:** Perfectly balanced dataset (50/50 split)

##  Tech Stack
- **Language:** Python 3.x
- **Core Libraries:** Pandas, NumPy, Scikit-learn, Scipy
- **Techniques:** NLP, Text Preprocessing, Bag of Words, Sparse Matrices, Logistic Regression

##  Key Features
- **Custom text preprocessing pipeline:** HTML removal, lowercasing, punctuation handling, tokenization
- **Manual Bag of Words implementation:** Built from scratch using sparse matrices (99,420 features)
- **Memory-efficient design:** Sparse matrix representation (5 billion cells → 500MB)
- **Logistic Regression classifier:** Trained on 40,000 reviews, tested on 10,000
- **Proper evaluation methodology:** 80/20 train/test split with stratification

##  What I Learned
- **NLP Fundamentals:** Text preprocessing, tokenization, and feature extraction
- **Memory Optimization:** Using sparse matrices to handle high-dimensional data efficiently
- **Model Evaluation:** Proper train/test splitting, avoiding overfitting, interpreting precision/recall
- **Trade-offs:** Balancing model complexity vs. interpretability
- **Debugging:** Solved word-merging issues in preprocessing pipeline

##  Results
```
Test Accuracy: 89.35%
Precision: 90% (Negative), 89% (Positive)
Recall: 89% (Negative), 90% (Positive)
F1-Score: 89% (Both classes)
```

**Example Predictions:**
- "This movie was absolutely amazing!" → Positive (87.4% confident) 
- "Waste of time. Boring and predictable." → Negative (98.6% confident) 
- "Great acting but terrible plot." → Negative (68.2% confident) 

##  Future Improvements
- [ ] Implement TF-IDF weighting for better feature representation
- [ ] Add n-grams (bigrams/trigrams) to capture phrase context
- [ ] Experiment with advanced models (SVM, Random Forest, LSTM)
- [ ] Build interactive web interface using Streamlit
- [ ] Add cross-validation for more robust evaluation

##  Project Structure
```
├── sentiment_analysis.ipynb    # Main Jupyter notebook with full pipeline
├── README.md                   # Project documentation (this file)
├── requirements.txt            # Python dependencies
└── .gitignore                  # Git ignore file
```

##  How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/Code-blize/imdb-sentiment-analysis.git
cd imdb-sentiment-analysis
```

### 2. Download the Dataset
Download the IMDB Dataset from [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) and save it as `IMDB Dataset.csv` in the project directory.

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Notebook
```bash
jupyter notebook sentiment_analysis.ipynb
```

##  Challenges & Solutions
| Challenge | Solution |
|-----------|----------|
| Word merging after HTML removal | Replaced tags with spaces instead of empty strings |
| Memory issues with 5B matrix cells | Used scipy sparse matrices (lil_matrix) |
| Mixed sentiment reviews | Accepted limitation; noted for future n-gram implementation |

##  Connect
Built by Obasi-Uzoma Blessing as part of Generative AI & Data Science internship preparation.

---

⭐ If you found this helpful, please star the repository!
