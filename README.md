# Fine-Tuning GPT-2 with LoRA (Low-Rank Adaptation)
This repository demonstrates how to fine-tune GPT-2 using the LoRA (Low-Rank Adaptation) technique with the Hugging Face Transformers library. LoRA enables efficient parameter updates by only training a small subset of the model's parameters, making it a lightweight and resource-efficient approach to fine-tuning large language models.

**Features**
LoRA Fine-Tuning: Efficient low-rank adaptation applied to GPT-2 for causal language modeling.
Dataset: BookCorpus (subset of 1000 samples).
Lightweight Training: Only LoRA parameters are updated, reducing memory and computational requirements.
Text Generation: Generates creative text using the fine-tuned GPT-2 model

**Prerequisites**
Ensure you have Python installed (>=3.8 recommended) along with the following libraries:

transformers
datasets
torch
peft

**Dataset**
The dataset used is BookCorpus, which consists of a large corpus of text data. This implementation uses a subset of 1000 samples for fine-tuning.

**Key Features of LoRA:**
Updates only a subset of GPT-2 parameters (low-rank layers).
Reduces memory usage and computational cost during training.
Effective for fine-tuning large language models for specific tasks.

**LoRA Configuration:**
Rank (r): 8
Scaling Factor (α): 32
Dropout: 0.1
Target Modules: c_attn and c_proj layers of GPT-2

**How to Run**
1. Clone the Repository:
git clone https://github.com/SriDharshana/gpt2-lora-finetuning.git  
cd gpt2-lora-finetuning

2. Install Dependencies:
pip install transformers datasets torch peft
     
3. Run the Script:
Fine-tune the GPT-2 model with LoRA by executing the script:
python fine_tune_gpt2_lora.py

4. Generate Text:
After training, use the generate_text function to generate text based on a prompt:

**Results**
The fine-tuned GPT-2 model generates coherent and creative text. LoRA enables efficient fine-tuning by focusing on low-rank updates, making it ideal for resource-constrained environments.
