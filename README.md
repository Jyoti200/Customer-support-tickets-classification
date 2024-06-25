# Customer-support-tickets-classification
We aim to create a model that categorizes customer complaints by the products or services involved. This will streamline ticket handling and lead to faster issue resolution.

# Data Preparation

Load the Data: Load the provided JSON data containing customer complaints.
Text Preprocessing: Perform preprocessing steps such as tokenization, removing stop words, lemmatization, and transforming text to lowercase.

# Topic Modelling with NMF
Vectorize the Text Data:
Use TF-IDF (Term Frequency-Inverse Document Frequency) to convert the text data into numerical format.
Use TfidfVectorizer from sklearn.feature_extraction.text.
Apply NMF (Non-Negative Matrix Factorization):
Initialize NMF with 5 components (since there are five categories: Credit card/Prepaid card, Bank account services, Theft/Dispute reporting, Mortgages/loans, Others).
Fit the NMF model on the TF-IDF matrix to extract topics.

# Interpretation of Topics
Identify Keywords for Each Topic:
For each component (topic), identify the top keywords that contribute to the topic.
Map these topics to the predefined categories based on the keywords.
Assigning Categories to Complaints

# Transform the Data:
Transform the TF-IDF matrix using the NMF model to get the topic distribution for each complaint.
Assign the Most Relevant Topic:
For each complaint, assign the category corresponding to the topic with the highest score.

# Supervised Learning Model
# Label the Data:
Use the topic modelling results to create a labelled dataset, where each complaint is associated with a category.

# Train a Supervised Model:
Split the labelled data into training and testing sets.
Train a supervised model (e.g., logistic regression, decision tree, or random forest) on the training data.

# Evaluate the Model:
Evaluate the model's performance using appropriate metrics (e.g., accuracy, precision, recall, F1 score) on the test data.
