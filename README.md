# European_Langugage_Detection
This project's aim is to compare three different language detection methods in order to find the most accurate one. These approaches are short word based, n-gram based and most frequent word based approaches. In each approach to make a prediction, first a bag of words for each language needs to be created. These bags contain top k frequent words or grams. In order to find the best k value I tried different ones during testing.
## Short Word Based
Here the definition of short word is a word with  or less letters. I extracted the short words for each language from the training set. Then looked into their frequencies in the language and put the top k frequent short words in that languages word bag. I created a word bag for each language. Then used these bags to predict the language of a new text. This prediction is done by a distance function. The language with the shortest distance is the predicted value.
## N-gram Based
N-gram based approach uses the same steps as the short word approach. It again uses distance function to predict the language of a new text. During testing as well as trying different k values I also had to try different n-grams to find the most accurate results.
## Most Frequent Word Based
In this approach I created the word bags based on the most frequent words of the languages train set. In order to make predictions I used the Multinomial Naive Bayes model. Later I also made the predictions with a random forest decision tree model to see which is a better choice.
## Testing 
After testing different k values. Most Frequent Word Based approach using MultinomialNB model turned out the be the best one. It is followed by Most Frequent Word Based approach using random forest model. Then the 2-grams is the best. Short word based approach turned out to be  worst.
