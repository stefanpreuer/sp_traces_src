---
title: Input preparation
---

Text is inherently sequential. It is a perfect fit for auto-regressive self-supervised learning, LLM excel in.

However text cannot be directly used, but instead it has to be prepared.

The input pipeline therefore has to:

1. Tokenize text

    Converting a sequence of text into a sequence of *token_ids* based on a vocabulary. 

2. Define embedding layer

    The embedding layer is an optimized layer doing weight based mapping of token_ids to multi-dimensional embedding vectors.

    During training it learns to produce embedding vectors representing semantical relation by vector similarity.

3. Integrate into data_loader abstraction

    For modularity input preparation has to be provided as data_loader abstraction. This allows integration with the further layers of the model.
