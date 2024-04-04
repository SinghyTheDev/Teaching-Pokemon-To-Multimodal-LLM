# Teaching Pokemon To Multimodal LLM

## Description
In this project the QLoRA method is used to fine-tune a pre-trained multimodal LLM from Hugging Face called IDEFICS-9B. The LLM is fine-tuned on a dataset consisting of Pokemon images and descriptions. Before, when prompted with a Pokemons image the pre-trained model demonstrated a very limited knowledge as it could only give the name of the Pokemon in the image. After training on the new data, when given the same prompts the model demonstrated a much deeper understanding of Pokemon including their type, HP, rarity, etc.

## Data Pre-Processing
Pre-processing carried out on the dataset includes random resized cropping (to prevent overfitting), normalisation of pixel values, and converting images to RGB format if they are not already in RGB format.

## Training
To prepare the pre-trained LLM for training it is quantized to 4-bit precision for efficiency. LoRA (Low Rank Adaptation) is then applied to enhance the models adaptability towards new data.

## Output
Before fine-tuning, when asked with Pokemon related image/text prompts the pre-trained model generated a very limited knowledge as it could only give the name of a Pokemon. After training on new data, when asked with the same prompts the model generated a much deeper understanding of Pokemon including their type, HP, rarity, etc.

## Conclusion
The fine-tuned LLM demonstrates enhanced knowledge of Pokemon compared to its initial state. This project showcases the training of multimodal models on domain-specific datasets to improve their performance in specific tasks. Larger datasets and further fine-tuning will likely yield even better results in the models ability to understand Pokemon.
