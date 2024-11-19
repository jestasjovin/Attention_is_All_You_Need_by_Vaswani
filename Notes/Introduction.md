### "Attention is All You Need" by Vaswani et al. (2017)

## Introduction
This paper introduces the Transformer architecture, which is the  backbone of various trending models in NLP, including GPT, BERT.

## Implementing the Transformer model from scratch

The intention is to understand how things are working on the

### 1. Transformer Architecture

The Transformer model architecture is made of mainly two parts

- **Encoder**
- **Decoder**

  **i. Encoder**
  The Encoder is responsible for processing the input sequence and generating a context representations for each token in the sequence. It also may have indentical layers stacked.

  - Consists of stacked two main layers
    1. Multi-Head Self-Attention
       \*allows the model to focus on different parts of the input sequence.
    2. Feedforward Neural Network
       \*position based network applied to each token.

