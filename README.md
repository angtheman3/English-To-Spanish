# English-To-Spanish

• Built seq2seq LSTM based translator using TensorFlow and Keras.      

• Streamlined data preprocessing using Pandas and regex.  

• Optimzed advanced training callbacks to enhance performance.  

# English to Spanish Neural Machine Translation (NMT) Using TensorFlow

## Overview

This project develops a Neural Machine Translation (NMT) model capable of translating English text into Spanish using a sequence-to-sequence (seq2seq) learning model with TensorFlow and Keras. This model uses Long Short-Term Memory (LSTM) networks and Embedding layers.

## Data Preprocessing

The dataset consists of English and Spanish sentence pairs. Preprocessing steps include:
- Lowercasing all text.
- Removing non-alphabetic characters.
- Adding start and end tokens to Spanish sentences.

## Vocabulary Creation

Vocabularies for both English and Spanish are created by iterating over each dataset and storing unique words.

## Sentence Length Analysis

Determines the maximum sentence length for both source (English) and target (Spanish) to set fixed lengths for input and output sequences.

## Model Architecture

### Encoder

- **Input Layer**: Takes variable-length sequences.
- **Embedding Layer**: Maps English words to a continuous vector space.
- **LSTM Layer**: Processes the embeddings with outputs and states passed to the decoder.

### Decoder

- **Input Layer**: Processes Spanish word sequences.
- **Embedding Layer**: Embeds Spanish words similarly to the encoder.
- **LSTM Layer**: Takes initial states from the encoder and outputs sequence predictions.
- **Dense Layer**: A softmax layer to generate probability distribution over the Spanish vocabulary.

## Training

- **Batch Generator**: Custom generator that yields batches of encoded sentences along with target sequences in a one-hot encoded format.
- **Loss Function**: Categorical crossentropy.
- **Optimizer**: RMSprop.
- **Callbacks**: ModelCheckpoint to save the best model and ReduceLROnPlateau to adjust the learning rate.

## Results

The model trains over 50 epochs, with training and validation loss monitored to prevent overfitting. The best model is saved and can be loaded for translation tasks.






