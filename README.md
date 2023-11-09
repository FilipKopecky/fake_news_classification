# Context: Course assignment
This is my solution for coding assignment in Supervised Learning course. We were supposed to find suitable dataset for NLP and then apply appropriate ML algorithms. I chose data set with fake news classification.

**What was the main goal?** Correctly classify unreliable news (fake news) and reliable news.

**What were tasks/steps to accomplish it?**
1. Preprocess the data.
2. Choose a suitable machine learning classifier.
3. Justify and explain the output.

# Data: News
Dataset called 'Fake News' is retrievable from [Kaggle](https://www.kaggle.com/competitions/fake-news/overview). It contains mix of unreliable and reliable news.

**Metadata:**
- **id**: unique id for a news article
- **title**: the title of a news article
- **author**: author of the news article
- **text**: the text of the article; could be incomplete
- **label**: a label that marks the article as potentially unreliable
    - **1**: unreliable
    - **0**: reliable

# Process and results
Comments on process are directly in the code. Here is quick overview:
1. Data load and simple Exploratory Data Analysis (EDA).
2. Data preprocessing phase, that included imputation of nulls values and standard NLP preprocessing stapes (removing stop words and multi-spaces, lowercasing, tokenization and lemmatization).
3. Vectorization using Bag of Words and TF-IDF methods.
4. Using Naive Bayes and Logistic Regression for classification.

Logistic Regression outperformed Naive Bayes in this task, as it has higher accuracy, precision and recall. The difference varied across changing alpha value of Naive Bayes model (0.04-0.11 in accuracy).

What looks suspicious is the exact same value of Logistic Regression model in all evaluation metrics. Even though my work was approved and no significant mistakes and issues were identified, I got suggestion to inspect this unusual occurrence.

**Thus, I drafted this to-do list for future work:**
1. Make and visualize confusion matrix.
2. Try cross-validation.