# Understanding the basics of BERT

## Introduction to BERT.

Natural Language Processing has seen huge improvements by training transformer-based language models on huge corpses of unlabelled data. For example, Wikipedia content.  

Then you fine-tune these models for downstream tasks like Question Answering, Text Summarization, Classification and so on.  

This form of pre-training by creating a supervised training task on unlabelled data is known as Self-Supervised Learning. Commonly seen in language modeling.  

Most language models are trained by iteratively predicting the next word in a sequence across enormous amounts of text.  

BERT presented a new self-supervised learning task for pre-training transformers in order to fine-tune them for downstream tasks.  

It’s a bi-directional transformer pre-trained using a combination of masked language modeling objective and next sentence prediction.  

It was proposed in the paper [“BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding”](https://arxiv.org/abs/1810.04805).  

