# email-classification-nlp
This project focuses on building a multi-class text classification system to categorize emails into different categories such as work, personal, spam, promotion and updates.
## Objective
To explore how machine learning models handle natural language data and to analyze their limitations in capturing semantic meaning.

## Approach

- Text preprocessing (lowercasing, cleaning)
- Feature extraction using TF-IDF
- Model training using Logistic Regression
- Evaluation using accuracy and confusion matrix

## Results

The model achieved an accuracy of approximately 73% on the test dataset.

## Analysis

The model performs well on clearly distinguishable categories such as work and updates, where specific keywords provide strong signals.

However, it struggles with semantically overlapping categories such as spam and promotion due to similar persuasive language patterns.

Additionally, some personal and update messages are misclassified as spam, highlighting the limitation of TF-IDF in capturing contextual meaning.

The model also shows a tendency to predict the "spam" class when uncertain, indicating reliance on keyword-based features rather than deeper semantic understanding.

## Limitations

- TF-IDF does not capture context or word order
- Small dataset size
- Difficulty in handling semantic ambiguity

## Future Improvements

- Use word embeddings (Word2Vec / GloVe)
- Experiment with transformer-based models like BERT
- Expand dataset with more diverse samples

## Technologies Used

- Python
- Scikit-learn
- Pandas
- Matplotlib / Seaborn
