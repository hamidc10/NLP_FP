# CS 662 Final Project

Fall 2023

Hamid Choucha & Anna Frederick

## Project Overview

Subject: Topic modeling of Amazon review data

Dataset: https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/

Models used:

- LDA (Hamid)
- BERTopic (Anna)

**Bertopic**
===

## Bertopic usage info:

### Environment for Bertopic

- BERTopic can be installed using pip.
- To use GPU acceleration for UMAP and hDBSCAN, you need to install RAPIDS cuML.
  - For specific installation info, please reference: https://docs.rapids.ai/install
    - Make sure you install for the proper CUDA version (11.6 on Cheaha)
    - Ensure you have the proper cupy version (cupy-cuda11x for Cheaha)
  - Non-GPU accelerated versions of these packages are available if needed.

### Scripts

- all files run the same overall training process (some hyperparameters may be tweaked)
  - `bertopic_giftcards.ipynb` will train on a small model of all giftcard reviews (~2000 reviews).
  - `bertopic_books.ipynb` will train a large model with 1 million book reviews.
  - `bertopic.ipynb` allows selecting and combining parts of different review datasets and training a model.
    - Does 500K sports/outdoors and 500K kitchen reviews by default

### Misc notes

- No saved models are uploaded, as they are very large.

## Citations:

- Justifying recommendations using distantly-labeled reviews and fined-grained aspects
  Jianmo Ni, Jiacheng Li, Julian McAuley
  Empirical Methods in Natural Language Processing (EMNLP), 2019
  
<br>

**LDA**
===

### Environment for LDA
- For LDA there was only one pip install to the already provided Environment that was given to use by Dr.Osborne
- Make sure to !pip install pyLDAvis it is in the first code block if you don't want to do it prior.
- As well as there is also nltk.download('brown') which is also on the first code block.

## LDA usage info:
-First you want to run Code Block 1 *Initialize the lda model*
-Second you want to run Code Block 2 *Grabbing the data from the database and make the .tar files into .json*
-Third you want to run Code Block 3 *This is used to condense the data into list*
-Finally you want to run Code Block 4 *This combines the data into one list as well cleans and tokenize them for use for the LDA model as well is used to initialize the data and make the html outputs*

### Scripts
-Just the Final LDA model that can be adapted and changed on the instance it is being run on as well as the what data the set the user want to use `Final LDA code.ipynb`


### Misc notes

- In code block 2 and 3 can be modified to only run certain dataset if wanting to test.
- In code block 4 make sure to update the number or works based on the number of cpu's used.
- As well as make sure to teak the number of topic based on how much data you are running on.

## Citations:

- Topic Modeling in Python: Latent Dirichlet Allocation (LDA)
'How to get started with topic modeling using LDA in Python'
    - (https://towardsdatascience.com/end-to-end-topic-modeling-in-python-latent-dirichlet-allocation-lda-35ce4ed6b3e0)
  
      Shashank Kapadia (Apr 14, 2019)

- Latent Dirichlet Allocation
  
    - (https://medium.com/analytics-vidhya/latent-dirichelt-allocation-1ec8729589d4)
  Harsh Bansal (Mar 3, 2020)

- PyDavis
  
  - (https://neptune.ai/blog/pyldavis-topic-modelling-exploration-tool-that-every-nlp-data-scientist-should-know)

