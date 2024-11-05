# InfoBot

A simple information driven chatbot that can engage in basic conversations with users, answering greetings, hospitality queries, and expressions of thanks. It can also attempt to respond to general queries using a provided text dataset.

## Features

- *Greetings*: Responds to common greetings such as "hello", "hi", etc.
- *Hospitality*: Responds to phrases like "how are you", "how you doing", etc.
- *Thanks*: Responds to expressions of gratitude such as "thank you", "thanks", etc.
- *General Queries*: Attempts to respond to user queries by analyzing a given text dataset using TF-IDF and cosine similarity.

## Pre-Requisites

The chatbot uses the following Python libraries:

- python version: 3.10.14
- random
- string
- requests: 2.32.3
- numpy: 1.26.4
- scikit-learn: 1.5.1
- nltk: 3.8.1

You can install the necessary packages using pip:

`pip install requests numpy scikit-learn nltk`

## Code Explanation

### 1. Downloading the Data

The python script allows the user to specifiy which text dataset to use for the chatbot, it allows the user to download and encode a new file from the web or use an existing text file for the dataset.

### 2. Pre-Defined Responses

The chatbot is designed to recognize certain user-inputs and respond with pre-defined outputs. These include Greetings, Hospitality and Gratitude inputs. The code includes lists of intents of user inputs and pre-defined responses for these intents. 

The `greeting(sentence)`, `hospitality(sentence)`, and `thanks(sentence)` functions checks if the user's input matches any keywords in their respective list of intents. If it does, it returns a random greeting response.

### 3. Text Processing and Response Generation

The text from the dataset is tokenzied into sentences and then into words, and also lemmatized. The respponse function generates a response by comparing the user's input with the dataset using TF-IDF and cosine similarity. It adds the user's input to the list of sentence tokens, computes the TF-IDF matrix, and finds the most similar sentence in the dataset.

### Main Loop 

The chatbot prompts the user to either download a new dataset or use an existing one. If the chatbot is activated, it interacts with the user, responding to greetings, gratitude, and queries based on the provided dataset until the user enters "bye".

## How to use

1. Run the script: Start the chatbot by running the script in your Python environment.
2. Choose the Dataset: Choose whether to download a new dataset/file or use an existing one.
3. Interact: Engage with the chatbot by typing your queries.
4. Exit: Type "Bye" to end the conversation.

## Notes

- To activate the chatbot, user input has to be 'yes' for the script to run.
- Dataset file must be a text file

  ---
