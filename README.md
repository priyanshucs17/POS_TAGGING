# POS_TAGGING

# HMMs and Viterbi algorithm for POS tagging

## Problem Statement:

You have learnt to build your own __HMM-based POS tagger__ and implement the Viterbi algorithm using the Penn Treebank training corpus. The vanilla Viterbi algorithm we had written had resulted in ~87% accuracy. The approx. 13% loss of accuracy was majorly due to the fact that when the algorithm encountered an unknown word (i.e. not present in the training set, such as 'Twitter'), it assigned an incorrect tag arbitrarily. This is because, for unknown words, the emission probabilities for all candidate tags are 0, so the algorithm arbitrarily chooses (the first) tag.

In this assignment, you need to __modify__ the Viterbi algorithm to solve the problem of unknown words using at least two techniques. Though there could be multiple ways to solve this problem, you may use the following hints:

-> Which tag class do you think most unknown words belong to? Can you identify rules (e.g. based on morphological cues) that can be used to tag unknown words? You may define separate python functions to exploit these rules so that they work in tandem with the original Viterbi algorithm.

-> Why does the Viterbi algorithm choose a random tag on encountering an unknown word? Can you modify the Viterbi algorithm so that it considers only one of the transition or emission probabilities for unknown words?

-> You have been given a '__test__' file below containing some sample sentences with unknown words. Look at the sentences and try to observe rules which may be useful to tag unknown words. Your final model will be evaluated on a similar test file.

## DATA:
For this assignment, you’ll use the __Treebank dataset of NLTK with the 'universal' tagset__. The Universal tagset of NLTK comprises only __12 coarse tag classes__ as follows: __Verb__, __Noun__, __Pronouns__, __Adjectives__, __Adverbs__, __Adpositions__, __Conjunctions__, __Determiners__, __Cardinal Numbers__, __Particles__, __Other/ Foreign words__, __Punctuations__.

__Note__: that using only 12 coarse classes (compared to the 46 fine classes such as NNP, VBD etc.) will make the Viterbi algorithm faster as well.

## Goals:
You can split the Treebank dataset into __train__ and __validation sets__. Please use a __sample size of 95:5 for training__: __validation sets__, i.e. keep the validation size small, else the algorithm will need a very high amount of runtime.

### You need to accomplish the following in this assignment:
1. Write the vanilla Viterbi algorithm for assigning POS tags (i.e. without dealing with unknown words) 

2. Solve the problem of unknown words using at least _two techniques_. These techniques can use any of the approaches discussed in the class - __lexicon__, __rule-based__, __probabilistic__ etc. Note that to implement these techniques, you can either write separate functions and call them from the main Viterbi algorithm, or modify the Viterbi algorithm, or both.

3. Compare the tagging accuracy after making these modifications with the vanilla Viterbi algorithm.

4. List down at least three cases from the __sample test file__ (i.e. unknown word-tag pairs) which were incorrectly tagged by the original Viterbi POS tagger and got corrected after your modifications.

 
PGDML_assignment
