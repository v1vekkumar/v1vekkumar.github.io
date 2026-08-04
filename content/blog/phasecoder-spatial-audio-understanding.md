---
title: "PhaseCoder: Geometry-Agnostic Spatial Audio for Multimodal LLMs"
date: 2026-01-25T10:00:00Z
draft: false
author: "Vivek Kumar"
description: "Overview of PhaseCoder, a transformer-based spatial audio encoder from Google DeepMind that enables multimodal LLMs to understand arbitrary microphone array geometries."
tags: ["spatial-audio", "deep-learning", "research", "DeepMind", "ICML"]
categories: ["Research"]
summary: "Overview of PhaseCoder — a transformer-based spatial audio encoder enabling multimodal LLMs to process arbitrary microphone array configurations."
ShowToc: true
---

> *Published at ICML 2026 / arXiv preprint [arXiv:2601.21124](https://arxiv.org/abs/2601.21124). Joint work with Artem Dementyev, Wazeer Zulfikar, Sinan Hersek, Pascal Getreuer, and Anurag Kumar at Google DeepMind.*

Multimodal Large Language Models (LLMs) can now process vision, text, and single-channel audio. But human hearing relies on **spatial sound** — using interaural time differences (ITD) and interaural level differences (ILD) to localize sources, separate overlapping speakers, and understand 3D scenes.

Standard audio encoders process single-channel or fixed-geometry stereo audio. In real-world environments (smartphones, smart home devices, robotics, automotive arrays), microphone geometries vary widely.

---

## What is PhaseCoder?

**PhaseCoder** is a transformer-based spatial audio encoder designed to be **geometry-agnostic**.

What it does:
1. **Arbitrary Array Processing**: Accepts raw multichannel audio along with 3D Cartesian coordinates of arbitrary microphone array geometries.
2. **Phase-Preserving Feature Extraction**: Encodes inter-channel phase relationships directly into continuous spatial embedding space without requiring pre-calibrated array geometry assumptions.
3. **Spatial Audio Tokens**: Outputs discrete or continuous spatial audio tokens that interface directly with frozen multimodal LLMs (e.g. Gemma family).

---

## Key Results & Capabilities

- **3D Sound Source Localization**: Accurately estimates azimuth and elevation of multiple concurrent sound sources.
- **Targeted Spatial Transcription**: Allows users to prompt the model with a spatial direction (e.g., *"Transcribe only the speaker to my left at 45 degrees"*), isolating the intended speech stream even in high background noise.
- **Zero-Shot Array Generalization**: Evaluated on unseen microphone array layouts during inference with zero performance degradation.

Read the full paper on [arXiv:2601.21124](https://arxiv.org/abs/2601.21124).
