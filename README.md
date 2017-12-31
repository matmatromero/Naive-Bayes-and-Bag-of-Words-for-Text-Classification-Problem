# Tweet-Classification-using-Naive-Bayes

A classic application of Bayes Law is in document classification. Let’s examine one particular classification
problem: estimating where a Twitter “tweet” was sent, based only on the content of the tweet itself. We’ll
use a bag-of-words model, which means that we’ll represent a tweet in terms of just an unordered “bag” of
words instead of modeling anything about its grammatical structure. </br></br>

We'll implement a Naive Bayes classifier for this problem. For a given tweet D, we’ll need to evaluate P (L =
l|w 1 , w 2 , ..., w n ), the posterior probability that a tweet was taken at one particular location (e.g., l = Chicago)
given the words in that tweet, making the Naive Bayes assumption, which says that for any i 6 = j, w i is
independent from w j given L. </br></br>
The dataset is of tweets labeled with their actual geographic locations, split into a training set and a testing set. the dataset is restricted to a set of a dozen North American cities (Chicago, Philadelphia, etc.), so the task is to classify each tweet into one of twelve different categories.
</br></br>
The program accepts command line arguments like this:
./geolocate.py training-file testing-file output-file
</br></br>
The program should then load in the training file, estimate the needed probabilities to build a Bayesian
model, and apply them to each tweet in the testing file, and then write the results into output-file. </br> </br>
The file format of the training and testing files is simple: one tweet per line, with the first word of the line indicating
the actual location. Output-file has the same format, except that the first word of each line is the estimated label, the second word is the actual label, and the rest of the line is the
tweet itself. </br></br>
The program also outputs (to the screen) the top 5 words associated with each of the 12
locations (i.e. the words for which P (L = l|w) is the highest for each l).
