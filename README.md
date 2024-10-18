# LLM-20-questions-game

This repository contains the implementation of an AI-based gamebot capable of playing the 20 Questions game using the Meta-Llama-3.1-8B-Instruct model. The gamebot asks yes/no questions and makes educated guesses based on user responses to identify a word within 20 questions.

## Project Overview

The **LLM-20 Questions Gamebot** is designed to interact with users through a series of yes/no questions to narrow down the category (place, person, or thing) of a chosen word. The goal is for the bot to guess the word correctly before 20 questions are exhausted.

The gamebot leverages the **Meta-Llama-3.1-8B-Instruct** model, a state-of-the-art language model built on transformer architecture, optimized for natural language understanding and generation.

### Key Features:
- Interactive guessing game using yes/no questions
- Designed to guess a word within 20 questions
- Built on the Hugging Face Transformers library
- Uses the Meta-Llama-3.1-8B-Instruct model with 8 billion parameters for advanced language processing

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Implementation Details](#implementation-details)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [Acknowledgements](#acknowledgements)

## Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/dheeraj932/LLM-20-questions-game.git
    cd LLM-20-questions-game
    ```

2. **Install dependencies:**
    Make sure you have Python 3.7+ installed, then install the required libraries

3. **Download the Meta-Llama-3.1-8B-Instruct model:**
    The model can be accessed from the Hugging Face model repository.
    ```bash
    from transformers import AutoModelForCausalLM, AutoTokenizer
    model = AutoModelForCausalLM.from_pretrained("meta-llama/3.1-8b-instruct")
    tokenizer = AutoTokenizer.from_pretrained("meta-llama/3.1-8b-instruct")
    ```

## Usage

1. **Start the game:**
    The gamebot will interact with the user in a loop for up to 20 rounds, asking questions and making guesses.

2. **Input:**
    The user must think of a word (person, place, or thing) and respond with yes/no to the gamebot's questions.

3. **End Condition:**
    The game ends when the gamebot correctly guesses the word or after 20 questions have been asked.

## Implementation Details

The project utilizes the **Meta-Llama-3.1-8B-Instruct** model for both generating questions and making guesses. Key architectural elements:
- **Transformer-based model:** Built on the self-attention mechanism.
- **Roles of the Gamebot:** The bot alternates between asking questions and making guesses.
- **Termination:** The game concludes if the correct guess is made or if 20 questions are exhausted.

## Results

During testing, the model was able to guess words like "Boston" correctly within 7 questions. The performance of the gamebot was generally satisfactory, though future improvements are noted for refining question generation and guessing accuracy.

## Future Improvements

1. **Refined Question Generation:** Enhancing prompt engineering to produce more effective and insightful questions.
2. **Adaptive Learning:** Implementing features for dynamic adjustment of questions based on previous answers.
3. **User Interaction Enhancements:** Adding more flexibility in user inputs and improving the overall interactive experience.

## Acknowledgements

This project was completed as part of CS6120 at Northeastern University, under the guidance of Professor Uzair Ahmad. Special thanks to the developers of the Hugging Face Transformers library for their powerful tools.
