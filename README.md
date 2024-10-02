# Similar Question Search Engine using BERT

## Table of Contents
- [Introduction](#introduction)
- [Technologies](#technologies)
- [Dataset](#dataset)
- [Model](#model)

## Introduction

This project implements a **Similar Question Search Engine** using **BERT** (Bidirectional Encoder Representations from Transformers). The purpose of this engine is to find the most semantically similar questions to a user query from a large dataset of previously asked questions. It leverages BERT to generate contextual embeddings for each question, which allows the model to better understand the meaning behind the text.

The engine is useful for:
- Identifying similar questions in customer support systems.
- Enhancing FAQ systems by quickly retrieving relevant answers.
- Improving user experience by reducing question duplication.
  
## Technologies

- **Python 3.8+**
- **BERT (Transformers)**
  - Hugging Face's `transformers` library for pre-trained BERT models.
- **NumPy** for vector operations.
- **Pandas** for dataset

## Dataset

**[Quora Question Pairs Dataset](https://www.quora.com/q/quoradata/First-Quora-Dataset-Release-Question-Pairs)**:
   - Contains pairs of questions and labels indicating whether the two questions are duplicates.
   - You can use either question column as your search database.

## Model

This project uses **DeBERTa-v3** (Decoding-enhanced BERT with disentangled attention) for generating embeddings of the questions. DeBERTa, developed by Microsoft, improves on the BERT architecture by using disentangled attention and enhanced positional encodings, resulting in better language understanding and representation capabilities.

### Why DeBERTa-v3?

DeBERTa-v3 is chosen for this project due to its superior performance over traditional BERT models, specifically in natural language understanding tasks. Key improvements include:
- **Disentangled Attention**: DeBERTa separately encodes content and position information, allowing the model to better understand the relative importance of different words in context.
- **Enhanced Positional Encodings**: Unlike standard sinusoidal positional embeddings in BERT, DeBERTa uses absolute and relative positional encodings to capture better context.
- **Pre-training Efficiency**: DeBERTa-v3 has been pre-trained on large amounts of data, enabling it to outperform previous models like RoBERTa and BERT on various benchmarks.

For this project, we use the **DeBERTa-v3-base** model, which balances performance and efficiency. The model is imported using the Hugging Face `transformers` library.
