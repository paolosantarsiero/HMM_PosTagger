# HMM_PosTagger

The project consists of developing a statistical morphological analyzer for ancient Greek and Latin, called POS Tagger, based on the Hidden Markov Model statistical technique, using two Treebanks from the UD project.
The development involves the implementation of four fundamental tasks:
* Learning and Decoding function
* Train the model
* Apply different smoothing strategies
* Evaluate the model

## Aims
* Learning: count the occurrences of each word and each tag present in the training file of both tree banks. Calculate the emission and transition probabilities, which are used later in the next step.
* Decoding with Viterbi algorithm.
* Train the model: With some accuracy and probability, tag the words of even a sentence in both Greek and Latin that the model has never seen.
* Smoothing strategy: apply different smoothing strategies when the model is faced with unknown words.
* Evaluate the model: this task, on the other hand, consists of using a baseline that allows you to evaluate and, consequently, compare the performance of the model on a test set. The result of this phase was to calculate the accuracy of the model and analyze the errors made.
