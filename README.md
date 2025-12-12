**DLProject — Character-Level Transformer Language Model**

This repository contains our implementation of the Deep Learning Mini Project for the course, where we build a decoder-only Transformer language model trained on the Tiny Shakespeare dataset.
The goal of the project is to understand and implement key components of the Transformer architecture from scratch, train the model, and generate Shakespeare like text.

**Repository Contents**
Below is a description of each file included:

DL-Mini project.pdf: Presentation slides- This PDF contains the final slides and forms the presentation portion of the project submission.

Instructions_file_miniproject2_language_model.ipynb: Official instructions provided by the professor

attempt1_Shakespearellm.ipynb:Initial attempt of the project which is the earlier version of the implementation. Kept for record but NOT the final version. Contains partial implementation and some corrections

mini_project_language_model.ipynb: FINAL submission notebook (complete and corrected implementation).This notebook contains the full working project and is the one for evaluation.

## What We Built

A GPT-style transformer with:
- 12 transformer layers
- 8 attention heads per layer
- 768 dimensional embeddings
- About 85 million parameters
- Trained on Shakespeare text

## Requirements

Python 3.8+ with these libraries:
```bash
pip install torch matplotlib
```

**Training time:**
- With GPU (Google Colab T4): approximately 4.5 hours
- With CPU: 10-12 hours or more

We trained on Google Colab's free tier which worked well.

## Dataset

We used the Tiny Shakespeare dataset:
- Contains Shakespeare's complete works
- 65 unique characters (letters, punctuation, spaces)
- Split: 90% training, 10% validation

Download from: [shakespeare.txt](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)

## Training Details

Key settings we used:
- Batch size: 128
- Context length: 128 characters
- Learning rate: 0.0001
- Training steps: 6000
- Dropout: 0.3

The model saves checkpoints during training and keeps the best one based on validation loss.

## Results

After training for 6000 steps:
- Best validation loss: 1.48 
- Final validation loss: 1.62
- Perplexity improved from 82 to 5

