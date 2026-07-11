# Fine-tuning LLaMA-2-7B using QLoRA on a Custom Dataset

This project demonstrates parameter-efficient fine-tuning of **Meta's LLaMA-2-7B** model on a custom text dataset using **QLoRA (Quantized Low-Rank Adaptation)**. By combining **4-bit quantization** with **LoRA adapters**, the project significantly reduces GPU memory requirements while adapting a 7B parameter language model to a domain-specific dataset.

---

## Overview

Large Language Models often require substantial computational resources for fine-tuning. This project explores an efficient fine-tuning pipeline that:

- Fine-tunes **LLaMA-2-7B** on a custom dataset
- Uses **QLoRA** with **4-bit NF4 quantization**
- Applies **LoRA adapters** for parameter-efficient training
- Keeps the base model frozen while training only adapter weights
- Performs instruction-based supervised fine-tuning using Hugging Face Transformers

---

## Key Features

- Fine-tuning of **Meta LLaMA-2-7B**
- QLoRA-based training
- 4-bit quantization using BitsAndBytes
- LoRA adapters on transformer attention layers
- Parameter-efficient fine-tuning (training only ~0.2% of model parameters)
- Hugging Face Transformers + PEFT
- Custom text dataset

---

## Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- PEFT
- BitsAndBytes
- Datasets
- Accelerate

---

## Model

**Base Model**

- Meta LLaMA-2-7B-Chat

**Fine-tuning Technique**

- QLoRA
- LoRA (Low-Rank Adaptation)

**Quantization**

- 4-bit NF4

---

## Training Configuration

| Parameter | Value |
|-----------|------:|
| Epochs | 3 |
| Learning Rate | 1e-4 |
| Batch Size | 2 |
| Gradient Accumulation | 2 |
| Quantization | 4-bit |
| Fine-tuning Method | QLoRA + LoRA |

---

## Project Workflow

```

Custom Dataset
│
▼
Tokenizer
│
▼
4-bit Quantization
(BitsAndBytes)
│
▼
LLaMA-2-7B
│
▼
LoRA Adapters
│
▼
Parameter-efficient Fine-tuning
│
▼
Fine-tuned Model

```

---

## Repository Structure

```

.
├── README.md
├── requirements.txt
└── finetuning\_personal\_dataset.ipynb

```

---

## Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git
```

Move into the project

```bash
cd <repository-name>
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
finetuning_personal_dataset.ipynb
```

---

## Dataset

The notebook uses a custom text dataset for supervised instruction fine-tuning.

Update the dataset path inside the notebook before training if using your own data.

---

## Results

The project successfully demonstrates:

- Memory-efficient fine-tuning of a 7B parameter LLM
- Parameter-efficient adaptation using LoRA
- Reduced GPU memory consumption through 4-bit quantization
- End-to-end training pipeline using the Hugging Face ecosystem

---

## Future Improvements

- Hyperparameter optimization
- Evaluation on benchmark datasets
- Experiment with larger LoRA ranks
- Multi-GPU training using DeepSpeed/FSDP
- Model deployment using Hugging Face Inference Endpoints

---

## License

MIT License

---

## Author

**Rishu Bhadani**

B.Tech, Mechanical Engineering  
Minor in Artificial Intelligence and Data Science  
Indian Institute of Technology Bombay
