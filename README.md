# English_to_Glosses
NMT for English to Glosses for English to Glosses to identify signs

## Problem:
The task is to create a model that can translate from english to glosses to identify the sign language.

## Dataset:
* There are two txt file for source (English) and target (Glosses).
* Source file contains the each sentence per line.
* Each line contains a number of word separated by whitespaces
* Target file contains the each sentence per line.
* Each line contains a number of word separated by comma

## Preprocessig 
* I escaped the unicode to read the data from the line
* Source data is normalized first
* Anything other than letters and numbers from source data is removed
* There is no prerocessing done for the target data since I have little knowledge about the sign language.

## Model
The NMT model consists of the following layers
* Encoder
* Attention
* Decoder

I passed the sequence of input to the model and it passes through each of the layer to translate a sentence.

There are feq hyperparameters that can be fine-tuned
* Embedding Dimension
* Number of Units
* Number of epochs

The model is trained using the trainining data

## Output
Finally I predict the text using a test data and write the output in the text file where tokens are separated by comma.
