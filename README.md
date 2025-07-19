# NanoGPT-Shakespeare

This is a basic reimplementation of the "Attention Is All You Need" paper, focused on the decoder-only transformer architecture used in GPT models. The model is trained from scratch on the Tiny Shakespeare dataset using character-level tokenization.

The code is written for readability and learning. It avoids high-level libraries or frameworks and builds the model components (multi-head attention, feedforward layers, positional embeddings, etc.) using raw PyTorch.

## Features

- Decoder-only transformer (GPT-style)
- Character-level tokenizer (custom encode/decode logic)
- Multi-head self-attention with causal masking
- Learned positional embeddings
- LayerNorm and residual connections
- Simple training loop using AdamW
- Generates text one character at a time

## Model details

- Embedding dimension: 128
- Number of heads: 4
- Number of layers: 4
- Context window (block size): 64
- Batch size: 16
- Dropout: 0.1
- Training steps: 9000

## Data

The model is trained on the Tiny Shakespeare dataset (a small corpus of Shakespeare text). Character-level tokenization is used instead of word or subword tokenization.

## Notes

The `train.py` file contains the full model implementation and training loop. It also includes many inline comments and side notes where I recorded my thoughts while learning and building the model. Some of these comments may be messy or unintelligible at times, as they were written in the moment during the learning process.
