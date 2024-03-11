---
layout: distill
title: Transformers
description: An in-depth look at the transformative impact of deep learning transformers on natural language processing (NLP). 
tags: distill formatting
giscus_comments: true
date: 2024-01-27
featured: true
published: false

authors:
  - name: Otto Vintola
    url: "ottovintola.github.io"
    affiliations:
      name: Aalto University

bibliography: 2024-01-27-TF.bib

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Equations
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Citations
  - name: Footnotes
  - name: Code Blocks
  - name: Interactive Plots
  - name: Layouts
  - name: Other Typography?

# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
---


## Introduction

In recent years, the field of natural language processing (NLP) has witnessed a monumental shift in its approach to handling textual data. Traditional methods, such as recurrent neural networks (RNNs) and convolutional neural networks (CNNs), while effective, struggled to capture long-range dependencies and suffered from vanishing gradient problems. However, the advent of deep learning transformers has marked a paradigm shift in NLP, enabling more efficient and effective modeling of sequential data.

## Understanding Transformers

Transformers, introduced by Vaswani et al. in the groundbreaking paper "Attention is All You Need," <d-cite key="bengio2014representation"></d-cite> represent a novel architecture that relies solely on self-attention mechanisms, eliminating the need for recurrent or convolutional layers. This architecture comprises an encoder-decoder framework, with multiple stacked layers, each consisting of self-attention mechanisms and feed-forward neural networks.

The key innovation of transformers lies in their ability to process input data in parallel, rather than sequentially, making them highly scalable and efficient. This parallelization is achieved through self-attention mechanisms, which allow the model to weigh the importance of different input tokens when generating output representations.

## Self-Attention Mechanism

The self-attention mechanism in transformers enables the model to weigh the relevance of each input token with respect to the others, thereby capturing long-range dependencies and contextual information. Given a set of queries, keys, and values, the self-attention mechanism computes a weighted sum of the values based on the similarity between the queries and keys.


## Advantages of Transformers

The rise of deep learning transformers in NLP can be attributed to several key advantages:

- **Parallelization:** Transformers can process input data in parallel, leading to significant speedups during training and inference compared to sequential models like RNNs.
- **Long-range Dependencies:** Transformers excel at capturing long-range dependencies in sequential data, making them well-suited for tasks requiring understanding of contextual information over extended sequences.
- **Transfer Learning:** Pre-trained transformer models can be fine-tuned on task-specific data with minimal effort, enabling transfer learning across a wide range of NLP tasks.
- **Attention Mechanisms:** The self-attention mechanism allows transformers to focus on relevant parts of the input sequence, facilitating better representation learning.

## Conclusion

Deep learning transformers have emerged as a cornerstone technology in the field of natural language processing, offering unparalleled performance across various tasks. With their ability to capture long-range dependencies, process data in parallel, and facilitate transfer learning, transformers have paved the way for groundbreaking advancements in NLP applications. As research in this area continues to evolve, we can expect transformers to play an increasingly pivotal role in shaping the future of language understanding and generation systems.

---

### Equations

$$
\text{Transformer architecture}
$$

$$
\text{Attention}(Q,K,V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
$$

$$
\text{MultiHead}(Q,K,V) = \text{Concat}(\text{head}_1, \dots, \text{head}_h)W^O
$$

$$
\text{head}_i
