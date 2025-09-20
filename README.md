# Fine-Tuning Vision-Language Models 🚀

This repository contains notebooks and use cases for fine-tuning state-of-the-art Vision-Language Models (VLMs) on custom datasets. All examples are designed to run on free Google Colab notebooks.

-----
## [Medium](https://medium.com/@elsayed_mohamed) 

vision language models  finetuning notebooks &amp; use cases
Vision Language Models (VLMs) are a cutting-edge type of artificial intelligence that combines computer vision and natural language processing. These models can understand and generate text based on visual inputs, bridging the gap between visual and textual information.

![PaliGemma](assets/pali1.png)


| Model | Notebook Link |
|-------|---------------|
| PaLIGemma | [Colab pali_gemma_OCR_Meter.ipynb]([https://github.com/sayedmohamedscu/Vision-language-models-VLM/blob/main/pali_gemma_OCR_Meter.ipynb](https://colab.research.google.com/github/sayedmohamedscu/Vision-language-models-VLM/blob/main/updated_pali_gemma_OCR_Meter.ipynb)) |
| Florence-2 | [Fine_tune_Florence_2_metere_values.ipynb]([https://github.com/sayedmohamedscu/Vision-language-models-VLM/blob/main/Fine_tune_Florence_2_metere_values.ipynb](https://colab.research.google.com/github/sayedmohamedscu/Vision-language-models-VLM/blob/main/Fine_tune_Florence_2_metere_values_updated.ipynb)) |
|MedGemma4b-it|[MedGemma4b Fine-Tuning Notebook](https://github.com/sayedmohamedscu/Vision-language-models-VLM/blob/main/medgemma_4b_it_prev.ipynb)|



## Key Features

1. Image Understanding: VLMs can analyze and interpret complex visual scenes.
2. Text Generation: Based on visual inputs, these models can generate relevant textual descriptions or responses.
3. Multi-modal Learning: VLMs can process and correlate information from both visual and textual sources.

How VLMs Work
Vision Language Models operate through a sophisticated process that combines several key components:

Image Encoder: The first step involves encoding the input image into a latent space representation. This is typically done using advanced image encoding models such as CLIP (Contrastive Language-Image Pre-training), SigLIP (Signal-based Language-Image Pre-training), PaLI (Pathways Language and Image model), or DINO (Self-Distillation with No Labels). These encoders transform the raw pixel data into a compact, high-dimensional vector that captures the image's salient features.
Latent Space Projection: The latent space representation from the image encoder needs to be aligned with the text embedding space. This is achieved through a projection layer, which is essentially an Artificial Neural Network (ANN). This projector maps the image embeddings to a space that is compatible with text embeddings.

Text Embedding Merger: Once the image embeddings are projected into the appropriate space, they are merged with the text embeddings. This process allows the model to create a unified representation that combines both visual and textual information.

Language Model: The merged embeddings are then processed by a language model, which can generate text based on the combined visual and textual input.

This architecture allows VLMs to perform tasks such as image captioning, visual question answering, and even generating text that is contextually relevant to both images and text prompts.




## Applications

VLMs have a wide range of applications, including:

- Image captioning
- Visual question answering
- Object detection and recognition
- Scene understanding
- Assistive technologies for visually impaired individuals

## Examples

## Example1 PaliGemma Finetuning

### Electronic Meter Reading




![Electronic Meter](assets/meter1.png)

In this image, a VLM could be trained to read the Meter values using henrik-dra/energy-meter dataset:
- Recognize the type of meter
- Read and interpret the digital display


## Example1 Florence2 Finetuning

### Electronic Meter Reading (same dataset)




![Electronic Meter](assets/Florence.png)

Florence-2 could be used with multiple otrher applications like detection , segmnenation ,OCR , OCR with bbox and image captionating.

Here are the Florence-2 tasks 

![Electronic Meter](assets/flo-tasks.png)
![Electronic Meter](assets/flo1.png)






-----



### MedGemma 4B: Fine-Tuning for Medical Vision 🩺

This project walks you through fine-tuning **MedGemma 4B**, Google's powerful multimodal model optimized for medical applications. MedGemma combines a **SigLIP** vision encoder with the **Gemma 3** architecture, making it highly effective at understanding complex medical images like chest x-rays.

In this guide, we use **QLoRA** to efficiently fine-tune the model on a custom medical dataset. This technique makes it possible to train a 4-billion-parameter model even on a free Colab notebook.

  * **Model**: `google/medgemma-4b-it`
  * **Technique**: QLoRA (4-bit Quantization + LoRA)
  * **Use Case**: Medical Visual Question Answering (VQA)

➡️ **Check out the full guide in the [MedGemma Fine-Tuning Notebook]([https://www.google.com/search?q=https://github.com/kingabzpro/vision_language_models_finetuning/blob/main/medgemma-qlora-finetune.ipynb](https://github.com/sayedmohamedscu/Vision-language-models-VLM/blob/main/medgemma_4b_it.ipynb)).**

-----

### Florence-2: Fine-Tuning for Document OCR

This project demonstrates how to fine-tune **Florence-2**, Microsoft's powerful vision model, which is excellent for a wide variety of vision tasks, especially those involving text on documents. Since the fine-tuning logic for this model is not yet integrated into the `transformers` Trainer, this notebook uses a custom PyTorch training loop.

Here, we fine-tune the small 232M parameter version to read values from energy meters.

  * **Model**: `microsoft/Florence-2-base-ft`
  * **Technique**: Standard fine-tuning with a custom PyTorch loop
  * **Use Case**: Document Visual Question Answering (DocVQA) / OCR

➡️ **Explore the code in the [Florence-2 Fine-Tuning Notebook](https://www.google.com/search?q=https://github.com/kingabzpro/vision_language_models_finetuning/blob/main/Florence-2-Fine-tuning.ipynb).**

-----

### PaliGemma: Meter Reading

This project covers fine-tuning **PaliGemma**, Google's lightweight and versatile VLM, for a custom task of reading energy meter values from images. It's a great example of applying a VLM to a specific OCR-style problem.

  * **Model**: `google/paligemma-3b-pt-224`
  * **Technique**: LoRA
  * **Use Case**: Optical Character Recognition (OCR) / Value Extraction

➡️ **Find the code in the [PaliGemma Meter Reading Notebook](https://www.google.com/search?q=https://github.com/kingabzpro/vision_language_models_finetuning/blob/main/paligemma_meter_reading.ipynb).**
