# Teaching Pokemon To Multimodal LLM

## Overview
Im this project the QLoRA method is used to fine-tune a pre-trained multimodal LLM from Hugging Face called IDEFICS-9B. The LLM is fine-tuned on a dataset consisting of Pokemon images and descriptions. Before, when prompted with a Pokemons image the pre-trained model demonstrated a very limited knowledge as it could only give the name of the Pokemon in the image. After training on new data, when given the same prompts the model demonstrated a much deeper understanding of Pokemon including their type, HP, rarity, etc.

## Data Pre-Processing
Transformations applied to the dataset include random resized cropping (to prevent overfitting) and normalisation of pixel values. Images are converted to RGB format if they are not already in RGB format.

## Training
To prepare the pre-trained LLM for training, it's quantized to 4-bit precision for efficiency. LoRA (Low Rank Adaptation) is then applied to enhance the models adaptability to new data.

## Output
Before fine-tuning, when prompted with Pokemon related image/text prompts the pre-trained model generated a very limited knowledge as it could only give the name of a Pokemon. After training on new data, when given the same prompts the model generated a much deeper understanding of Pokemon including their type, HP, rarity, etc.

## Conclusion
The fine-tuned LLM demonstrates enhanced knowledge of Pokemon compared to its initial state. This project showcases the training of multimodal models on domain specific datasets to improve their performance in specific tasks. Larger datasets and further fine-tuning will likely yield even better results in the models ability to understand Pokemon.
