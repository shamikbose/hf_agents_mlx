# Agents Course on Apple Silicon
This repository contains notebooks to replicate the learning from the wonderful [HF Agents Course](https://huggingface.co/agents-course), but to run locally on your Apple Silicon machine.

## Fine-tuning for function calling
`mlx_finetune` finetunes an instruct model [Llama-3.2-3B-Instruct](https://huggingface.co/meta-llama/Llama-3.2-3B-Instruct) for tool calling using the template presented in the [Colab notebook](https://colab.research.google.com/drive/1KwLr-ZeHBhLXeYFpkQaBDAEUIW8th8Fq?usp=sharing) in the [bonus unit](https://huggingface.co/learn/agents-course/bonus-unit1/introduction) of the course. 

Changes:
1. Llama-3.2 instead of Gemma-2. For some reason, Gemma-2 crashes using the MLX framework. There's an ongoing issue [here](https://github.com/ml-explore/mlx-examples/issues/664)
2. Storing data locally. This is required for the command-line LoRA tuner
3. Splitting data into train/validation/test. This lets you test the finetuned model's perplexity before and after tuning. 

