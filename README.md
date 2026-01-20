# Fine-Tuned Open-Source LLM for Product Price Prediction (QLoRA)

## Overview
This project demonstrates fine-tuning an open-source Large Language Model (LLM) for **product price prediction** using **QLoRA (Quantized Low-Rank Adaptation)**.  
The goal was to achieve **frontier-level performance** while significantly reducing training cost and memory usage.

The final fine-tuned model is evaluated on real-world product data and, in several cases, matches or outperforms larger proprietary models.

---

## Key Features
- Fine-tuning open-source LLMs using **QLoRA**
- Parameter-efficient training with low VRAM requirements
- End-to-end training → evaluation → inference pipeline
- Modular evaluation framework for price prediction tasks
- Emphasis on **cost–performance trade-offs** in real deployments

---

## Project Structure

Fine-Tuned Open-Source LLM for Product Price Prediction (QLoRA)/
├── day1.ipynb # Dataset exploration & problem formulation
├── day2.ipynb # Training setup & preprocessing
├── day3 and 4.ipynb # QLoRA fine-tuning pipeline
├── day5.ipynb # Final evaluation & inference (main notebook)
├── pricer/
│ ├── evaluator.py # Evaluation logic & metrics
│ └── items.py # Product schema & feature handling
├── util.py # Shared helper utilities
├── results.ipynb # Analysis of predictions & outputs
└── README.md


---

## Technical Approach

### Model Fine-Tuning
- Used **QLoRA** to fine-tune a quantized open-source LLM
- Enabled training on limited hardware by:
  - 4-bit quantization
  - Low-rank adapters (LoRA)
- Carefully tuned:
  - learning rates
  - rank dimensions
  - adapter placement

### Why QLoRA?
- Reduces memory footprint drastically
- Preserves model quality
- Makes fine-tuning feasible on consumer-grade GPUs

---

## Evaluation
- The model predicts product prices based on structured + textual inputs
- Performance evaluated using:
  - prediction accuracy
  - error distribution
  - comparison against baseline and frontier models
- Results show **competitive performance at a fraction of the cost**
