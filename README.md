# LoRA Fine-Tuning for Letter Counting

## Project Overview

This project demonstrates parameter-efficient fine-tuning of a Large Language Model (LLM) using **LoRA (Low-Rank Adaptation)** on a **Letter Counting** task.

The project compares the performance of the original pretrained model and the fine-tuned model using Chain-of-Thought prompting and reinforcement learning reward functions.

---

## Objectives

- Apply LoRA using the PEFT library
- Perform one-shot Chain-of-Thought prompting
- Design reward functions
- Fine-tune the model
- Monitor reward during training
- Compare pretrained and fine-tuned models

---

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- PEFT
- TRL
- Google Colab

---

## LoRA Configuration

| Parameter | Value |
|-----------|-------|
| Rank (r) | 16 |
| Alpha | 32 |
| Dropout | 0.05 |
| Bias | none |
| Task | Causal Language Modeling |

Target Modules

- q_proj
- k_proj
- v_proj
- o_proj

---

## Dataset

A small synthetic dataset containing letter-counting tasks.

Example

Input

Count the number of letter "a" in:

banana

Output

3

---

## Reward Functions

The following reward functions are implemented.

- Correctness Reward
- Counting Reward
- Formatting Reward
- Numbering Reward
- Spelling Reward

---

## Training Workflow

Dataset

↓

Baseline Prompting

↓

LoRA Configuration

↓

Reward Functions

↓

Fine-Tuning

↓

Reward Monitoring

↓

Model Evaluation

---

## Results

The notebook compares

- Original Model
- Fine-tuned Model

using identical prompts.

---

## Folder Structure

```
LoRA-Letter-Counting/
│
├── README.md
├── Letter_Counting_LoRA.ipynb
├── config.py
├── reward_functions.py
├── train.py
├── inference.py
├── requirements.txt
└── dataset/
```

---

## Author

Your Name
