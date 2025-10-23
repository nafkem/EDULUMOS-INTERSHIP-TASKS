Task 05: Sentiment Analysis on Amazon Reviews
Project Overview

This project analyzes Amazon product reviews to determine the overall sentiment expressed by customers.
It takes raw customer feedback, processes it, and classifies each review into Positive, Negative, or Neutral sentiment categories.
Through visualization and machine learning, the project mirrors how businesses extract insight from customer opinions to improve products and user experience.

🎯 Learning Objectives

I gained hands-on experience with:

1. Text Data Cleaning and Preprocessing
2. Exploratory Data Analysis (EDA) for NLP
3. Feature Engineering with TF-IDF
4. Machine Learning for Text Classification
5. Model Evaluation and Visualization

📂 Dataset

Name: Amazon Product Reviews (dummy dataset)
Input columns:

reviewText — textual review content
overall — numeric rating (1–5)

Output labels:
1–2 → Negative
3 → Neutral
4–5 → Positive

| Step | Phase                    | Description                                                                        |
| ---- | ------------------------ | ---------------------------------------------------------------------------------- |
| 1    | **Data Loading**         | Read CSV using Pandas and validate structure                                       |
| 2    | **Data Cleaning**        | Remove noise, punctuation, stopwords, and lemmatize words                          |
| 3    | **Feature Engineering**  | Convert text into numeric TF-IDF features                                          |
| 4    | **EDA**                  | Visualize class balance and key words using bar charts and word clouds             |
| 5    | **Modeling**             | Train Logistic Regression and Naive Bayes models                                   |
| 6    | **Evaluation**           | Compute accuracy, precision, recall, F1-score, and confusion matrix                |
| 7    | **Deployment Artifacts** | Save trained model (`sentiment_model.pkl`) and vectorizer (`tfidf_vectorizer.pkl`) |
| 8    | **Prediction Examples**  | Test sample reviews and output predicted sentiment                                 |

| Tool                         | Role in the Project                                          |
| ---------------------------- | ------------------------------------------------------------ |
| **Pandas**                   | Load and manipulate the dataset                              |
| **NumPy**                    | Handle numerical arrays and metrics                          |
| **Matplotlib & Seaborn**     | Plot sentiment distribution and confusion matrices           |
| **WordCloud**                | Visualize frequent words for each sentiment                  |
| **re (Regex)**               | Clean unwanted characters and symbols from text              |
| **nltk**                     | Tokenization, stopword removal, and lemmatization            |
| **scikit-learn**             | TF-IDF vectorization, model training, and evaluation metrics |
| **Pipeline**                 | Combine preprocessing and modeling steps                     |
| **joblib**                   | Save trained model and vectorizer for reuse                  |
| **imbalanced-learn (SMOTE)** | Balance dataset by oversampling minority classes             |


Key Visualizations

Sentiment Distribution – Bar chart of positive, neutral, and negative review counts
Word Clouds – Frequent words in positive and negative reviews
Confusion Matrix – Model prediction accuracy visualized in a heatmap

Model Performance
Two models were trained and evaluated:

| Model                   | Accuracy | F1 Score         | Notes      |
| ----------------------- | -------- | ----------------------------- | ---------------
| **Logistic Regression** | High     | Balanced precision and recall | Robust baseline model        |
| **Naive Bayes**         | Moderate | Faster, simpler alternative   | Useful for quick prototyping |

Run the following commands once to install all dependencies:

pip install pandas numpy scikit-learn nltk matplotlib seaborn wordcloud joblib imbalanced-learn


Optional (for advanced text embeddings):

pip install transformers torch sentence-transformers

💻 How to Run
Place your dataset in the project folder as amazon.csv
Run the main script:
python sentiment_analysis_amazon_reviews.py


View:
Model metrics and reports in console
Plots inline (sentiment distribution, word clouds, confusion matrix)

Saved model artifacts:

sentiment_model.pkl
tfidf_vectorizer.pkl

🧩 Example Predictions

sample_reviews = [
    "I love this product, it works perfectly!",
    "It's okay but not great.",
    "Terrible quality, broke after one use."
]


Predicted outputs:

Positive
Neutral
Negative

📚 Learning Outcome

After completing this project, i understood:

-How to clean and preprocess raw text data
-How to visualize and explore sentiment patterns
-How to train and evaluate NLP classification models
-How to interpret confusion matrices and evaluation metrics

-File Outputs

    File	                                Description
-sentiment_model.pkl	                    Trained Logistic Regression model
-tfidf_vectorizer.pkl	                Saved TF-IDF transformer
-amazon.csv	                            Input dataset
-sentiment_analysis_amazon_reviews.py	Main script
-README.md	                            Project documentation

Future Enhancements

Incorporate transformer-based models (BERT, DistilBERT)
Add sentiment intensity scores
Build a small web app using Streamlit or Flask for live review analysis


🚀 How to Push to GitHub (Step-by-Step)
Initialize Git
git init


Add your project files
git add sentiment_analysis_amazon_reviews.py amazon.csv README.md
Commit changes
git commit -m "Initial commit - Sentiment Analysis on Amazon Reviews"
Add the remote and push

git remote add origin https://github.com/nafkem/Sentiment-Analysis-Amazon-Reviews.git
git branch -M main
git push -u origin main