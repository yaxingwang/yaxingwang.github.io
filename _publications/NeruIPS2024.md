---
title: "Faster Diffusion: Rethinking the Role of the Encoder for Diffusion Model Inference"
collection: publications
permalink: /publication/NeruIPS2024
excerpt: ''
date: 2023-01-01
authors:
  - 'Senmao Li'
  - 'Taihang Hu'
  - 'Joost van de Weijer'
  - 'Fahad Shahbaz Khan'
  - 'Tao Liu'
  - 'Linxuan Li'
  - 'Shiqi Yang'
  - 'Yaxing Wang'
  - 'Ming-Ming Cheng'
  - 'jian Yang'
venue: '38th Conference on Neural Information Processing Systems (NeurIPS 2024)'
paperurl: 'https://proceedings.neurips.cc/paper_files/paper/2024/file/9ad996b5c45130de2bc00b60d8607904-Paper-Conference.pdf'
rawciteurl: 'http://yaxingwang.github.io/files/NeruIPS2024/citation.txt'
---

One of the main drawback of diffusion models is the slow inference time for image generation. Among the most successful approaches to addressing this problem are distillation methods. However, these methods require considerable computational resources. In this paper, we take another approach to diffusion model acceleration. We conduct a comprehensive study of the UNet encoder and empirically analyze the encoder features. This provides insights regarding their changes during the inference process. In particular, we find that encoder features change minimally, whereas the decoder features exhibit substantial variations across different timesteps. This insight motivates us to omit encoder computation at certain adjacent time-steps and reuse encoder features of previous time-steps as input to the decoder in multiple time-steps. Importantly, this allows us to perform decoder computation in parallel, further accelerating the denoising process. Additionally, we introduce a prior noise injection method to improve the texture details in the generated image. Besides the standard text-to-image task, we also validate our approach on other tasks: text-to-video, personalized generation and reference-guided generation. Without utilizing any knowledge distillation technique, our approach accelerates both the Stable Diffusion (SD) and DeepFloyd-IF model sampling by 41% and 24% respectively, and DiT model sampling by 34%, while maintaining high-quality generation performance.
