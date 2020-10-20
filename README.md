# Hidden Markov Model Project

## Description
This project was a part of the Udacity Natural Language Processing Nanodegree. Here, you can see my solutions to Part of Speech Tagging, using their suggested models. The motivation for this project is to leverage bigram word counts, and already labelled text data, with parts of speech. The idea is to create an HMM that can predict the parts of speech, given a string of text.
## File Structure

- |- `hmm-tagger.html`
- |- `hmm-tagger.ipynb`

## Hidden Markov Model

### Most Frequent Classifier
* The first model simply creates an embedded dictionary where this is true: `pair_counts[NOUN][time] == 1244`.
* In other words, this model simply relies on frequency for making predictions on P.O.S. , and the accuracy is fairly high, above 90%.
* What about when a word's P.O.S. is aambiguous, like *dis*-count the noun, and dis-*count* the verb ?

### Unigram and Bigram Counts

* This part does not define its own model, but helps to build to creating a custom HMM.
* Firstly, unigram counts defines a dictionary as such `your_unigram_counts[NOUN] == 275558`.
* The next step is to nest this dictionary, with words parts of speech that occur in the same phrase. (This helps to define transition probability for the HMM.

### Sequence starting and ending counts

* Leveraging the probabilities above for when words transition between each other (in the middle of a sentence), the last step for the HMM transitions is to observe the beginning/end of each sequence as well.
* Lastly, the HMM will be created where each of these transition likelihoods are discrete distributions.
* Prediction here was above 95%!





