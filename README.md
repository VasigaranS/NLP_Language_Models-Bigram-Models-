# NLP_Language_Models-Bigram-Models-
A (statistical) language model predicts the probability of the next word, based on the preceding words.


You can use the -d option to save the model to file, e.g. :
python BigramTrainer.py -f data/kafka.txt -d kafka model.txt

Also reading a model and a test corpus, and computing the entropy of the test corpus given the model 

The script run tester small kafka.sh tests the model built from small.txt using kafka.txt as a test corpus, and the script run tester kafka small.sh tests the model build from kafka.txt on the test corpus small.txt and generates cross entropy.
