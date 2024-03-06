# Restaurant-Review-Analysis-using-NLP-in-R
Project showcases sentiment analysis on restaurant reviews, employing text mining techniques and a random forest classifier. It utilizes packages like tm, randomForest, and caTools for preprocessing, feature extraction, and classification, aiming to predict review sentiments as positive or negative.
Project serves as a comprehensive exploration of sentiment analysis applied to restaurant reviews. It begins by reading in a tab-separated value (TSV) file containing the reviews data. The text mining (tm) package is then employed to create a corpus from the reviews column, followed by several preprocessing steps. These steps involve converting text to lowercase, removing numbers and punctuation, stemming words to their root forms, eliminating common stopwords, and stripping extra whitespace.

Once the text is processed, a document-term matrix (DTM) is generated to represent the frequency of terms in the corpus. Sparse terms, i.e., those appearing in less than 0.1% of the documents, are removed from the DTM. The resulting DTM is converted into a data frame named "reviews," where each row corresponds to a review and each column to a term frequency.

The sentiment of each review is labeled as either liked (1) or not liked (0), and the data frame is split into training and test sets using the caTools package. A random forest classifier is trained on the training set to predict the sentiment of reviews in the test set.

After making predictions on the test set, a confusion matrix is generated to evaluate the performance of the classifier. The confusion matrix provides insights into the accuracy of the predictions, including the number of true positives, true negatives, false positives, and false negatives.

Overall, this notebook demonstrates a step-by-step approach to sentiment analysis on textual data, showcasing the use of text mining techniques and machine learning algorithms for classification tasks.
