# TinyGpt
This repository contains an implementation of TinyGPT, a small-scale GPT model created from scratch.

## Key Points :

Architecture: TinyGPT is built upon the transformer architecture, which is widely used in natural language processing tasks. It consists of a stack of identical decoder blocks, each containing self-attention mechanisms and feed-forward neural networks.

Self-Attention: The self-attention mechanism allows the model to weigh the importance of different words in the input sequence when generating the output. It enables the model to capture contextual dependencies effectively.

Decoder Blocks: TinyGPT comprises multiple decoder blocks stacked on top of each other. Each decoder block consists of a self-attention layer, a feed-forward neural network, and layer normalization. The self-attention layer attends to the previous positions in the sequence, capturing the interdependencies between different tokens.

Attention Dropout: To improve the generalization capability of the model, attention dropout is applied during training. This technique randomly drops out a certain percentage of attention weights, encouraging the model to learn more robust representations.

Embedding Dropout: Embedding dropout is used to regularize the model during training. It randomly sets a certain percentage of the token embeddings to zero, preventing overfitting and enhancing the model's ability to generalize.

<div align="center">
  <img src="images/new_tinygpt.png" alt="figure">
</div>


## Configuration

<div align="center">

| Setting            | Value |
| ------------------ | ----- |
| attn_dropout       | 0.1   |
| embed_dropout      | 0.1   |
| ff_dropout         | 0.1   |
| vocab_size         | 100   |
| max_len            | 20    |
| num_heads          | 12    |
| embed_dim          | 768   |
| num_decoder_blocks | 12    |

</div>
