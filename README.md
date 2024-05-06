# NLP-Projects
This is a repository dedicated to showcasing projects developed using Natural Language Processing (NLP) techniques. From sentiment analysis to text generation, this repository features various NLP applications.

<img src="https://github.com/daunyl/NLP-Projects/assets/137568373/b477cdb4-47e4-4323-a9f5-20c7110abae1">

## 1. [NER Model](https://github.com/daunyl/NLP-Projects/tree/main/NER%20Model)
<img src="https://github.com/daunyl/NLP-Projects/assets/137568373/f0a9e759-bad9-4ac6-8318-3627e5e0a926" width="500" height="300">

This Named Entity Recognition (NER) model is one of my initial projects in Natural Language Processing (NLP), built primarily with TensorFlow. Leveraging TensorFlow's straightforward syntax and rich set of functions, this project was both a learning experience and a practical tool for identifying named entities within text.

### Examples of Real-world Applications:
1. **Information Extraction**: Extracting names of people, organizations, and locations from news articles, enabling quick summarization and analysis.
2. **Resume Parsing**: Identifying key information such as skills, experiences, and contact details from resumes, aiding in automated recruitment processes.
3. **Medical Record Analysis**: Recognizing entities like diseases, treatments, and patient names from medical records, facilitating medical research and patient care.
And a lot more.


## 2. [The Siamese model](https://github.com/daunyl/NLP-Projects/tree/main/Siamese%20Model)
is designed to determine whether pairs of questions are duplicates or not. Here's a breakdown of its structure:
<img src="https://github.com/daunyl/NLP-Projects/assets/137568373/af2399c7-7924-4a4d-9f4d-1adf060238d7" width="500" height="300">


### 5 Layers:
- `Text Vectorization`: This layer processes the input text and converts it into numerical representations.
- `Embedding Layer`: Converts the numerical representations into dense vectors of fixed size, which capture semantic information about the words.
- `LSTM (Long Short-Term Memory)`: A recurrent neural network layer that processes sequences of data, capturing dependencies between words in the text.
- `Global Average Pooling 1D`: Aggregates the output of the LSTM layer across time steps, providing a fixed-length representation of the entire input sequence.
- `Lambda Layer`: Normalizes the output vector to unit length using L2 normalization, which helps in making the model robust to variations in input length.


`Input Layers`:
Two input layers, each taking a single string as input (input_1 and input_2).
### Model Architecture:
Both inputs are processed through the same set of layers, making use of weight sharing.
The model architecture follows the siamese approach, where two identical branches process each input separately, and their outputs are then concatenated.
Concatenation Layer:
Concatenates the outputs of the two branches along the feature dimension (axis=1), producing a single feature vector representing both inputs.

**This Siamese model is a powerful tool for identifying duplicate questions, with its ability to learn nuanced similarities between pairs of questions.**

## 3. [Neural Machine Translation (NMT) Project](https://github.com/daunyl/NLP-Projects/tree/main/Neural%20Machine%20Translation)
<img src="https://github.com/daunyl/NLP-Projects/assets/137568373/59e0e0f4-7c06-46f0-b1ea-9e1a4e8cf95e" width="500" height="500">

This project implements a Neural Machine Translation (NMT) model for translating text from one language to another. The architecture comprises an encoder and a decoder, both utilizing Long Short-Term Memory (LSTM) networks with attention mechanisms.

### Model Architecture:

- **Encoder**:
  - The encoder processes the input sentence to create a fixed-length representation.
  - **Embedding Layer**: Maps words to dense vectors, capturing semantic information.
  - **Bidirectional LSTM**: Captures contextual information from both directions of the input sequence.

- **Decoder**:
  - The decoder generates the output sentence based on the encoder's representation and previously generated tokens.
  - **Embedding Layer**: Converts the input tokens into dense vectors.
  - **Pre-Attention LSTM**: Processes the input tokens while maintaining hidden and cell states.
  - **Attention Mechanism**: Focuses on relevant parts of the input during decoding.
  - **Post-Attention LSTM**: Processes the attended output from the encoder.
  - **Output Layer**: Produces probabilities of each token in the target vocabulary using a softmax function.

- **Translator Model**:
  - Combines the encoder and decoder into a single model.
  - Takes a tuple of input context (source sentence) and target (shifted-to-the-right translation) as input.
  - Generates log probabilities of each token in the target vocabulary.

### Model Usage:
1. **Training**: Train the model on parallel corpora with source-target language pairs.
2. **Inference**: Translate sentences by passing the source sentence through the encoder and decoding the output using beam search or greedy decoding.

### Example Application:
- **Translation of Text**: Translating sentences from one language to another, enabling cross-lingual communication and understanding.

This NMT project provides a powerful tool for automated translation, with its ability to capture complex patterns and dependencies in language data.
