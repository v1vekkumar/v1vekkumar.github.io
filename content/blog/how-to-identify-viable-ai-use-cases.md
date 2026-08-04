---
title: "How to Identify Viable AI Use Cases"
date: 2020-11-20T10:00:00Z
draft: false
author: "Vivek Kumar"
description: "A practical framework for founders and investors to evaluate whether an AI use case is viable, defensible, and worth building — from data flywheels to compute constraints."
tags: ["AI", "strategy", "angel-investing", "startups"]
categories: ["AI Strategy"]
summary: "A framework for founders and leaders to evaluate practical AI applications vs hype."
ShowToc: true
---

Every product team wants to add AI these days. But not every problem needs deep learning, and many proposed AI features fail because the task is a poor fit for ML.

As an AI researcher and angel investor, here is the mental model I use to evaluate whether a proposed AI use case makes sense.

---

## 1. High Noise, High Volume, Low Latency Requirement

AI models excel when data volume is massive, patterns are complex or noisy, and rule-based heuristics break down.

- **Good AI Use Case**: Real-time acoustic noise suppression or spatial audio rendering where classical DSP filters struggle with non-stationary background noise.
- **Bad AI Use Case**: Fixed conditional workflow logic that can be written in 10 lines of deterministic code.

## 2. Tolerance for Probabilistic Outputs

Machine learning models produce probabilistic outputs. A viable use case must account for error bounds:
- **High-Tolerance Domains**: Creative generation, audio synthesis, recommendation engines, search rank.
- **Low-Tolerance Domains**: Safety-critical systems without human-in-the-loop guardrails.

## 3. Data Flywheel & Feedback Loop

The best AI products create a virtuous cycle:
$$\text{User Interaction} \rightarrow \text{Data Collection} \rightarrow \text{Model Refinement} \rightarrow \text{Better Product}$$

Ask: *Does using the product naturally generate clean, labeled ground-truth signal to fine-tune the model over time?*

## 4. Compute Constraints & Edge Deployment

Evaluating an AI project requires asking *where* the model will run:
- Cloud-hosted foundation models (high parameters, high latency tolerance).
- On-device edge models (strict memory, battery, and real-time latency budgets).

Designing for compute efficiency early prevents expensive production refactoring later.
