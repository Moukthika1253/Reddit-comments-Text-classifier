# Reddit-comments-text-classifier
## Loading Dataset
Upload the csv files Top_Posts.csv and Top_Posts_Comments.csv to the content folder in google collab.Import pandas library.

converted both csv files into post_df and comment_df. Merged them together on common column post_id into dataframe target_df.

Splitted the target_df into Train (50%), Development(20%) and Test dataset(30%).

I have removed the null values or empty rows from all three datasets because when I trained my model without removing null values I got an error. 

Then I have preprocessed the training data by removing stopwords, punctuations, tokenized the words, removed extraspaces and lemmatized the words.

Later I created a dictionary word_dict and stored the word frequencies for each category artificial, MachineLearning, datascience. 

Then I have calculated the probabilities of P(artificial), P(MachineLearning), P(datascienece) and their prior probabilities P(word|MachineLearning), P(word|artificial), P(word|datascience).I used these to finally calculate probabilities P(artificial|word), P(MachineLearning|word), P(artificial|word). 

I have calculated probabilities over different alphas and predicted classes. Calculated accuracy for dev and test dataset with this NaiveBayes classifier.

Then I have split my training data into train, test and dev dataset to reduce the data.

Then I have vectorized training data and converted to tf-idf form.

Used classifiers KNN, SVm, Logisitic Regression, Decision Tree and Random Forest by importing libraries from sklearn.

Experimented with various hyperparameters and calculated dev and test accuracies. Visualized those using graphs from seaborn.

Finally compared test accuracies of all classifiers.
