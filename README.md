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

# Encoder Flow

1. **Embed** each word into a vector (using an embedding layer).
2. **Add Positional Encoding** to each word embedding adds word's position in the sequence.
3. For each Encoder Layer
   - **Self-Attention** Compute attention between all words.
   - **Feedforward Network**

After processing through all Encoder Layers, the final embeddings will contain rich contextual information about each word in relation to all others in the sequence.

# **Multi-Head Self-Attention**
* How does this works
- **Self-attention** this enables each token to have information on the context of the entire sequence.
- **Multi-head attention** computes multiple attention scores in parallel Using different learned set of weights of queries, keys, and values. Each head captures different context sequence.




**Math behind Self-Attention**

Self-attention computes the attention for each token \( t_i \) in the sequence by using _queries, values and key_, which are all derived from the input sequence.

- The attention score is calculated as how much is the query similar to all keys.

The formula for Scaled Dot-Product Attention

\[
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right) V
\]

Where

- \( Q \) is the query matrix.
- \( K \) is the key matrix.
- \( V \) is the value matrix.
- \( d_k \) is the dimensionality of the key vectors.
- The softmax function is applied over the dot product of \( Q \) and \( K^T \), scaled by \( \sqrt{d_k} \).
