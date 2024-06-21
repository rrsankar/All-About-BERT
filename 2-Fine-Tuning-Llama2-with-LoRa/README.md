# Fine-Tuning Llama-2 LLM with LoRa

## Goal
The goal of this project was to understand the fine-tuning process of a Large Language Model, specifically Llama 2.

## Base Model
The base model used here is from HuggingFace - [NousResearch/Llama-2-7b-chat-hf](https://huggingface.co/NousResearch/Llama-2-7b-chat-hf).

## Dataset
The dataset used here is also from HuggingFace - [mlabonne/guanaco-llama2-1k](https://huggingface.co/datasets/mlabonne/guanaco-llama2-1k)

## Llama 2 Overview
Open-source foundation model from Meta.  
Check more at [Github](https://github.com/meta-llama/llama) & [HuggingFace](https://huggingface.co/docs/transformers/en/model_doc/llama2).  
There are 2 different versions:  
Llama-2: Pre-Trained LLM with 7b, 13b & 70b parameter variants.  
Llama-2-chat: LLM optimized for dialog using RLHF. Also has 7b, 13b & 70b parameter variants.  

## What is PEFT & LoRA? How does it help in Fine-Tuning?
PEFT stands for Parameter Efficient Fine-Tuning, a fine-Tuning strategy which requires less computation power without losing much model performance, compared to fine-tuning the whole model.  
One of the PEFT techniques is LoRA and it stands for Low Rank Adaptation.  
LoRA does a low rank decomposition by representing a weight matrix as two smaller matrices.  
The idea is that if we lose the linearly dependent columns from the weight matrix, we can reduce the computation (since there are less weights to tune now) without losing much information.  
This is done by using a rank hyperparameter ‘r’.  
The weights in the smaller matrices are updated while Back Propagation depending on our new dataset.  
In a nutshell, instead of fine-tuning the whole weight matrix, we tune 2 smaller matrices.  
In the end, the fine-tuned weights are added to the original model.

## Conclusion
This project achieved its goal of helping me understand the nuances in LLM fine-tuning process.  
This will serve as a base work for other LLM fine-tuning experiments.  

## Reference
[Hugging Face documentation](https://huggingface.co/docs)
[Article-KDNuggets](https://www.kdnuggets.com/fine-tuning-llamav2-with-qlora-on-google-colab-for-free)
