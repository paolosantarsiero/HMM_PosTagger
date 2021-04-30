# HMM_PosTagger

The project consists of developing a statistical morphological analyzer for ancient Greek and Latin, called POS Tagger, based on the Hidden Markov Model statistical technique, using two Treebanks from the UD project.
The development involves the implementation of four fundamental tasks:
* Learning and Decoding function
* Train the model
* Apply different smoothing strategies
* Evaluate the model

## AIMS
* Learning: count the occurrences of each word and each tag present in the training file of both tree banks. Calculate the emission and transition probabilities, which are used later in the next step.
* Decoding with Viterbi algorithm.
* Train the model: With some accuracy and probability, tag the words of even a sentence in both Greek and Latin that the model has never seen.
* Smoothing strategy: apply different smoothing strategies when the model is faced with unknown words.
* Evaluate the model: this task, on the other hand, consists of using a baseline that allows you to evaluate and, consequently, compare the performance of the model on a test set. The result of this phase was to calculate the accuracy of the model and analyze the errors made.

## SMOOTHING ENUMERATION
* 0 => no smoothing
* 1 => P(unk|NOUN) = 1
* 2 => P(unk|NOUN) = 0.5 and P(unk| VERB) = 0.5
* 3 => P(unk|tag) = 1/ #(tagset)
* 4 => POS Statistics, only words with one occurrence
* 5 => Lemma Statistics, use lemma to learning task

## ACCURACY ON GREEK
Smoothing type             | Accuracy
-------------------------- | --------------------------
No smoothing  | 0.729090128345818
P(unk|NOUN) = 1 | 0.7366763681473353
P(unk|NOUN) = 0.5 and P(unk| VERB) = 0.5 | 0.7550455651510091
P(unk|tag) = 1/ #(tagset) | 0.729090128345818
POS Statistics | 0.7580514337516103
Lemma Statistics | 0.729090128345818

## ACCURACY ON LATIN 
Smoothing type             | Accuracy
-------------------------- | --------------------------
No smoothing | 0.9514099422733502
P(unk|NOUN) = 1 | 0.9514099422733502
P(unk|NOUN) = 0.5 and P(unk| VERB) = 0.5 | 0.9536940902861415
P(unk|tag) = 1/ #(tagset) | 0.9552722289131609
POS Statistics | 0.958220856347855
Lemma Statistics | 0.9552722289131609

### Python Dependences
* Jupyter notebook
* nltk
* conllu
* numpy



