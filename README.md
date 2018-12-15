# cs410explain
## Learn to explain Non-Standard English Words and Phrases

# Objective

The goal of this project is to build a model that learns to explain new, non-standard English expressions in a given sentence. 
Such cases are very frequent in social media, where language deviates from the formal use (abbreviations, slang, misspellings). 
Given a text sequence, the task is to automatically generate a definition/explanation of the specific parts of the text.
Original idea based on paper by Ke Ni and William Yang Wang (https://arxiv.org/pdf/1709.09254.pdf)

# Methodology - Our Model

The approach was to implement a seq2seq model presented in the original paper, and modify it to improve it wherever possible. 

[Model Implementation in Google Colab](https://colab.research.google.com/drive/1Q039vkRUqwI3U6uxXZNP87_XaKNAki1d) (CS410_Explain.ipynb)

![Model implementation](https://github.com/yonguno/cs410explain/blob/master/seqseq.PNG)

# Framework

Implementation: PyTorch neural networks were run on Google Colaboratory to leverage their computational resources.

Training dataset: Urban Dictionary entries

Evaluation: 

    *Qualitative: Does the explanation make grammatical sense?
    *Quantitative: BLEU score

# Challenges

Computational resources: the model is very memory intensive and could not be run successfully on local machines, so Google Colab had to be used.

Large training set: the training dataset was very large and was too time consuming to iterate while exploring different model parameters, so a subset of the training set was used. 

Non-existent words: One of the challenges was the fact that the goal is to explain words that do not exist in real life and are hard to interpret. 

Misspellings and non-standard vocabulary in training set: Even the explanations from the training set were sometimes grammatically incorrect, had spelling errors, or used made-up words.


# Team Contributions
Yongwoo Noh
* Implemented original model with Pytorch
* Implemented BLEU score algorithm
* Performed model evaluations 
* Came up with POS tagging implementation

David Najera
* Implemented Bahdanau model (did not make it to the final implementation)
* Evaluated hyperparameter performance
* Performed initial research
* Helped with final implementation
