# Fine-tuning on Personal Dataset


## Overview
This repository contains a Jupyter Notebook for fine-tuning a model on a personal (custom) dataset. The notebook walks through data loading, preprocessing, model configuration, training, and evaluation.

## Tech Stack
- Pytorch
- Huggingface

## Requirements
Install dependencies (adjust versions as needed):

```bash
pip install datasets peft torch transformers GPUtil google huggingface_hub
```

### Notebook-Embedded Installs
The notebook also includes these installation commands (review/merge with requirements above):

```
!pip install peft
!pip install accelerate
!pip install bitsandBytes
!pip install transformers
!pip install datasets
!pip install GPUtil
```

## Dataset
**Hugging Face Datasets used:** text

**Local dataset paths referenced:**
- /content/Fine-tuning-LLMs/data/hawaii_wf_2.txt
- /content/Fine-tuning-LLMs/data/hawaii_wf_4.txt

**Data/model files referenced:**
- /content/Fine-tuning-LLMs/data/hawaii_wf_2.txt
- /content/Fine-tuning-LLMs/data/hawaii_wf_4.txt

## Model & Training
**Base / checkpoint candidates detected:** ./finetunedModel, ./log, /content/Fine-tuning-LLMs/data/hawaii_wf_2.txt, /content/Fine-tuning-LLMs/data/hawaii_wf_4.txt, finetunedModel/checkpoint-20, meta-llama/Llama-2-7b-chat-hf

**Hyperparameters observed:**
- **epochs**: 3
- **learning_rate**: 1e-4
- **batch_size**: 2
- **train_batch_size**: 2
- **gradient_accumulation_steps**: 2

**Output directories:** ./finetunedModel

## How to Run

1. Clone or download this project and ensure the dataset paths in the notebook are correct.
2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # on Windows: .venv\Scripts\activate
   ```
3. Install dependencies (see **Requirements**).
4. Launch Jupyter and open the notebook:
   ```bash
   jupyter lab  # or jupyter notebook
   ```
5. Execute cells top-to-bottom, monitoring GPU/CPU memory and logs.


## Results
Add key metrics (e.g., accuracy, F1, loss curves) and sample predictions.

## Repository Structure
- `finetuning_personal_dataset.ipynb` — main notebook.
- `README.md` — this file.
- `data/` — place your dataset here (optional).
- `outputs/` — trained artifacts/checkpoints (optional).

## Reproducibility
- Set random seeds where applicable.
- Pin package versions or use a lockfile/`requirements.txt`.
- Log training config and metrics (e.g., with TensorBoard or Weights & Biases).

## License
Specify your license (e.g., MIT) here.
