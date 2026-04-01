Text Classification using Machine Learning

🧠 Overview

This project builds a multi-class text classification system to categorize messages into:

- Work
- Personal
- Spam
- Promotion
- Updates

The goal is not only to achieve high accuracy but also to understand model behavior, limitations, and generalization across different evaluation settings.

---

📂 Dataset

The dataset consists of manually curated text messages across five categories.

To evaluate model robustness, three datasets were used:

- Standard/Test Dataset → Regular evaluation
- Balanced Dataset → Equal representation of all classes
- Hard Dataset → Ambiguous and tricky messages

---

🧹 Preprocessing

- Text cleaning (lowercasing, normalization)
- TF-IDF vectorization
- Conversion of text into numerical features

---

🔀 Train-Test Split

The dataset was split into:

- Training set → used for model training and analysis
- Test set → used for final evaluation

---

🤖 Models Used

- Logistic Regression
- Multinomial Naive Bayes
- Linear Support Vector Classifier (Linear SVC)

---

🔤 Feature Engineering (Bigrams)

In addition to unigram features, bigram features were introduced:

TfidfVectorizer(ngram_range=(1,2))

💡 Insight

- Bigrams capture short context (e.g., “call now” vs “call me”)
- Improved performance on structured data
- Mixed results on harder datasets due to increased feature complexity

---

📊 Evaluation

🟢 Test Dataset

- High accuracy (~90%+) across models
- Linear SVC performs best

---

⚖️ Balanced Dataset

- Consistent performance across classes
- Provides fair evaluation without class bias

👉 Models perform well when class distribution is uniform

---

⚠️ Hard Dataset

- Accuracy drops significantly (~60–70%)

👉 Indicates:

- difficulty handling ambiguous inputs
- reliance on surface-level patterns

---

📈 Learning Curve Analysis

Learning curves were generated using 5-fold cross-validation to study model behavior with increasing data.

🔍 Observations

- All models improve with more data
- Linear SVC achieves the best performance
- Logistic Regression shows stable improvement
- Naive Bayes performs well with small data but plateaus early

---

🔍 Training vs Validation

- Training accuracy is higher than validation accuracy
- Small gap → good generalization
- Linear SVC shows slight overfitting but still performs best

---

💥 Key Insights

- High accuracy on test data does not guarantee real-world performance
- Models struggle with ambiguous and mixed-intent messages
- Feature engineering (bigrams) improves context but may reduce generalization
- Data quality and diversity are as important as model choice

---

✅ Conclusion

- Traditional ML models perform well on structured text data
- Linear SVC is the best-performing model overall
- Naive Bayes is efficient for smaller datasets
- Performance drops on complex inputs highlight limitations of TF-IDF approaches

---

🚀 Future Work

- Use transformer-based models (e.g., BERT)
- Expand dataset with more diverse and realistic samples
- Improve handling of ambiguous and overlapping categories


- Model comparison
- Learning behavior
- Generali
