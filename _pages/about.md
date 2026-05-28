---
permalink: /
title: "Fan Jiang — LLM Fine-tuning & Efficient Adaptation"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a third-year undergraduate at **Yuanpei College, Peking University**, majoring in **General Artificial Intelligence**. My research interests lie at the intersection of efficient adaptation and deployment of large language models (LLMs), with a focus on **parameter-efficient fine-tuning (PEFT)**, **model architecture design**, and **LLM quantization / compression**.

I am particularly interested in how we can improve the **expressiveness and efficiency** of model updates under practical constraints such as limited compute, memory, and inference latency. Recent projects include distributed orthogonal adaptation for fine-tuning and cross-layer structured pruning methods for attention modules.

## Research Interests

- Parameter-efficient fine-tuning (PEFT) for LLMs  
- Model architecture design and efficient adaptation  
- LLM quantization, pruning, and inference-time efficiency  
- Distributed and structured optimization for foundation models  

## Publications

**HD-PiSSA: High-Rank Distributed Orthogonal Adaptation**  
Yiding Wang, Fanxu Meng, Xuefeng Zhang, **Fan Jiang**, Pingzhi Tang, Muhan Zhang  
*arXiv preprint*, 2025.  
[[Paper](https://arxiv.org/abs/2505.18777)] [[DOI](https://doi.org/10.48550/arXiv.2505.18777)]

Existing PEFT methods such as LoRA and PiSSA constrain updates to low-rank subspaces, which can limit expressiveness on complex tasks. We propose **HD-PiSSA**, a distributed PEFT approach that initializes orthogonal adapters across devices and aggregates their delta updates on the pre-trained weight matrix. By assigning different principal components to each GPU, HD-PiSSA expands the effective update rank and achieves strong gains on mathematics, code generation, and multi-task benchmarks.

**CLOVER: Cross-Layer Orthogonal Vectors Pruning and Fine-Tuning**  
Fanxu Meng, Pingzhi Tang, **Fan Jiang**, Muhan Zhang  
*arXiv preprint*, 2024.  
[[Paper](https://arxiv.org/abs/2411.17426)] [[DOI](https://doi.org/10.48550/arXiv.2411.17426)]

Decoder-only models suffer from growing KV-cache memory during autoregressive inference. We introduce **CLOVER**, which treats pairs of attention layers as low-rank decompositions via SVD on $Q\text{-}K$ and $V\text{-}O$ pairs within each head. The resulting singular values can guide pruning or serve as trainable parameters for efficient fine-tuning, enabling strong compression and performance improvements across language, speech, and vision-language models.
