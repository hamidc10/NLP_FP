# CS 662 Final Project

Fall 2023

Hamid Choucha & Anna Frederick

## Project Overview

Subject: Topic modeling of Amazon review data

Dataset: https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/

Models used:

- LDA (Hamid)
- BERTopic (Anna)

## Bertopic usage info:

### Environment

- BERTopic can be installed using pip.
- To use GPU acceleration for UMAP and hDBSCAN, you need to install RAPIDS cuML.
  - For specific installation info, please reference: https://docs.rapids.ai/install
    - Make sure you install for the proper CUDA version (11.6 on Cheaha)
    - Ensure you have the proper cupy version (cupy-cuda11x for Cheaha)
  - Non-GPU accelerated versions of these packages are available if needed.

### Scripts

- `bertopic_giftcards.ipynb` will train on a small model of all giftcard reviews (~2000 reviews).
- `bertopic_books.ipynb` will train a large model with 1 million book reviews.


### Misc notes

- No saved models are uploaded, as they are very large.

## Citations:

- Justifying recommendations using distantly-labeled reviews and fined-grained aspects
  Jianmo Ni, Jiacheng Li, Julian McAuley
  Empirical Methods in Natural Language Processing (EMNLP), 2019
