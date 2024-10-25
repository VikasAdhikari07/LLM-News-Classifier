# Text Categorization Project Using `facebook/bart-large-mnli` Model

This repository contains a project for text categorization, using the `facebook/bart-large-mnli` language model from Hugging Face.

## Project Overview

The project showcases text classification capabilities without the need for a labeled dataset, using zero-shot and few-shot learning. The `facebook/bart-large-mnli` model is used for natural language inference (NLI), identifying the most probable category for each input text based on provided category labels.

### Categories Used

The model is set to classify inputs into the following predefined categories:
1. Politics and Governance
2. Business and Economy
3. Technology and Science
4. Sports and Entertainment
5. Health and Lifestyle
6. World News and Social Issues

## Features

- **Zero-Shot Classification**: Classify text into categories without a labeled training dataset.
- **Few-Shot Learning with Examples**: Enhance the model’s categorization by including example sentences.
- **API Integration**: Utilize Hugging Face’s inference API for efficient text classification.

## Getting Started

### Prerequisites

- **Python 3.7+**
- **Hugging Face Transformers library**
- **Hugging Face API Token**: You need an API token from Hugging Face to use the `facebook/bart-large-mnli` model endpoint.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/VikasAdhikari07/LLM-News-Classifier.git
   cd LLM-News-Classifier
   ```
2. Install dependencies:
   ```bash
   pip install requests
   ```

3. Set up your Hugging Face API token:
   - Get a token from [Hugging Face](https://huggingface.co/settings/tokens).
   - Replace `YOUR_HUGGINGFACE_API_KEY` in the code with your API token.


### Customization

- **Adding Categories**: Extend the `categories` list with new domains relevant to your application.

## File Structure

- **README.md**: Project documentation.
- **main.ipynb**: Python notebook which contains the main code for setting up prompts and making API requests.

## Results and Limitations

This project demonstrates that even without labeled data, accurate text categorization can be achieved using zero-shot learning. However, performance may vary with complex or ambiguous input texts.
