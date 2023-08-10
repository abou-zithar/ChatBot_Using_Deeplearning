# Chatbot Training Code
This repository contains code for training a simple chatbot using a neural network model. The chatbot is designed to understand user intents and respond accordingly.

## Prerequisites
Before running the code, ensure you have the following libraries and tools installed:

- copyreg
- random
- json
- pickle
- numpy
- nltk
- tensorflow.keras
- google.colab (for mounting Google Drive)
You can install these libraries using the following command:

```bash

pip install copyreg random json pickle numpy nltk tensorflow keras google-colab
```
Additionally, you need to download NLTK data by running the following code within your Python environment:

- python
```bash
import nltk
nltk.download('wordnet')
nltk.download('omw-1.4')
nltk.download('punkt')
```
## Data Preparation
The code reads intent data from a JSON file (intents.json) located in Google Drive. Make sure you have the correct file path and that the file structure matches the expected JSON format.

## Training Process
Tokenization and Lemmatization: The code tokenizes and lemmatizes words from intent patterns using NLTK's WordNetLemmatizer. This reduces words to their root form for better understanding.

- Bag-of-Words Creation: The script creates a bag-of-words representation for each document (intent pattern) by encoding the presence or absence of words in a binary format.

- Model Architecture: The neural network model is built using TensorFlow Keras. It consists of three dense layers with dropout layers to prevent overfitting.

- Model Compilation: The model is compiled using the categorical cross-entropy loss function and the stochastic gradient descent (SGD) optimizer.

- Training: The model is trained using the training data generated from the bag-of-words and corresponding intent labels. Training accuracy and loss are displayed during each epoch.

- Model Saving: Once training is complete, the trained model is saved as ChatBot_model.hs.

## Usage
Clone this repository to your local machine.
Make sure you have the required libraries installed.
Replace the path to the intents.json file with your Google Drive path.
Run the code.
```bash
python chatbot_training_code.py
```
## Notes
The code uses deprecated functions and might need updates to work with newer versions of libraries.
This code provides a basic example of chatbot training and can be extended with more complex architectures and techniques for better performance.
Feel free to modify and experiment with the code to create a more advanced chatbot system.

##### Disclaimer: This README assumes you have a good understanding of Python programming and machine learning concepts. If you're new to these topics, consider learning more before diving into this code.

