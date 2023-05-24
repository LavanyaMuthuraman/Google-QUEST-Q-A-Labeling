---
# Google QUEST Q&A Labeling

#### Improving automated understanding of complex question answer content
---

### **Problem Statement**

Computers are really good at answering questions with single, verifiable answers. But humans are often still better at answering questions about opinions, recommendations, or personal experiences.

Humans are better at addressing subjective questions that require a deeper, multidimensional understanding of context - something computers aren't trained to do well…yet... Questions can take many forms - some have multi-sentence elaborations; others may be simple curiosity or a fully developed problem. They can have multiple intents, or seek advice and opinions. Some may be helpful and others interesting. Some are simply right or wrong.

<img alt="iwild" src="https://gatherup.com/wp-content/uploads/2018/01/Google-QA-logo-slide.png" width="600px"/>


**The [Google Quest Q/A labelling](https://www.kaggle.com/competitions/google-quest-challenge/overview) is a Kaggle competition where participants are expected to develop predictive algorithms for different subjective aspects of question-answer from Stack Exchange. Here, Subjective aspects are human-labelled to reflect whether the question-answer is well-written, relevant, helpful, etc.**


### Data Fields
 
The [Google QUEST Q&A Labeling Dataset ](https://www.kaggle.com/competitions/google-quest-challenge/data) consists of question-answer pairs sourced from various online platforms. The dataset is designed to improve the understanding and labeling of complex question-answer content. Here is a description of the key components of the dataset:

- Train data has total of 6079 rows and 41 columns where 11 columns are features and 30 columns are labels. Test data has a total of 11 columns only for features.

- The data is taken from the Kaggle competition which includes questions and answers from various StackExchange properties. Our task is to predict the target values of 30 labels for each question-answer pair. Target labels with the prefix question_ relate to the question_title and/or question_body features in the data. Target labels with the prefix answer_ relate to the answer feature.

- Each row contains a single question and a single answer to that question, along with additional features. The training data contains rows with some duplicated questions (but with different answers). The test data does not contain any duplicated questions.

- Target labels are aggregated from multiple raters, and can have continuous values in the range [0,1]. Therefore, predictions must also be in that range.


In this notebook involves performing exploratory data analysis on categorical and text features, engineering features for question and answer aspects, implementing machine learning models including Random, KNN, Logistic Regression, Random Forest, and XGBoost, computing average and weighted average of model predictions, and evaluating models using Spearman's correlation coefficient.

Finally, Best **Spearman's correlation coefficient is 0.8205** achieved using weighted average of K-Nearest Neighbour, Logistic Regression, Random Forest and XGBoost.
- Random Forest Algorithm outperformed all the models with SCC of 0.7979.
- Since each aspect has discrete set of values, classification performed better than regression.
- Since classes are of increasing order, there is possibility exact porobability is little deviatd to next or previous number.
- Hence, Accuracy Score off by 1 seems more uselfull than exact Accuracy Score.
