# Indian Name Transliteration using Sequence-to-Sequence Models

This project implements a sequence-to-sequence (Seq2Seq) model to transliterate Indian names from their English representation into Hindi. The task is handled using character-level conditional language models built with Recurrent Neural Networks (RNNs) and an Attention mechanism.

## Project Overview

The core of this project involves training a model to understand the phonetic and structural mapping between English and Hindi characters in the context of names. It explores two primary architectures:
1.  A standard **Encoder-Decoder RNN (GRU-based)**.
2.  An enhanced **Encoder-Decoder RNN with Bahdanau-style Attention**.

### Key Features
- **Custom BPE Tokenizer:** A Byte-Pair Encoding (BPE) tokenizer is trained from scratch for both the source (English) and target (Hindi) languages to handle the unique character sets and sub-word units effectively.
- **Model Training:** A model-agnostic trainer class is implemented to handle training loops, checkpointing, and evaluation for different architectures.
- **Evaluation Metrics:** The models are evaluated on Accuracy, Character Error Rate (CER), Token Error Rate (TER), and BLEU score.
- **Decoding Strategies:** The project includes implementations for both **Greedy Search** and **Beam Search** decoding to generate translations.

##  Tech Stack

- **Python**
- **PyTorch**
- **NumPy** & **Pandas** for data manipulation
- **NLTK** for BLEU score evaluation
- **Matplotlib** for visualizing attention maps

## Results

Both the standard RNN and the attention-based models were trained and evaluated. The attention mechanism provides insights into how the model learns to align characters between the two languages. The performance was measured on a validation set, showcasing the effectiveness of deep learning for this transliteration task.
