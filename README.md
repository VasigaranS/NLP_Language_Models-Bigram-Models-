# NLP_Language_Models-Bigram-Models-
A (statistical) language model predicts the probability of the next word, based on the preceding words.


You can use the -d option to save the model to file, e.g. :
python BigramTrainer.py -f data/kafka.txt -d kafka model.txt

Also reading a model and a test corpus, and computing the entropy of the test corpus given the model 

The script run tester small kafka.sh tests the model built from small.txt using kafka.txt as a test corpus, and the script run tester kafka small.sh tests the model build from kafka.txt on the test corpus small.txt and generates cross entropy.

Note that the model file is of the format:
• The first line contains two numbers, separated by space: The vocabulary size V (= the number of unique tokens, including punctuation), and the size of the corpus N (= the total number of tokens).
• Then follows V lines, each containing three items: an identifier (0, 1, . . .), a token, and the number of times that token appears in the corpus.
• Then follows a number of lines, one for each non-zero bigram probability. Each line contains three numbers: The identifiers of the first and second token of the bigram, respectively, followed by the logarithm of the bigram probability, printed with 15 decimals. The natural logarithm is used (as computed by the math.log library method).
• The final line is “-1” to mark end-of-file.
