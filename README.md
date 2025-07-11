# Urdu Text Generation with Deep Learning

This project demonstrates character-level and word-level Urdu text generation using deep learning models (LSTM, GRU, and SimpleRNN) in TensorFlow/Keras. The models are trained on a corpus of Urdu text to generate new, coherent Urdu text sequences.

## Features

- **Character-level and word-level text generation**
- Supports **LSTM**, **GRU**, and **SimpleRNN** architectures
- Includes **data preprocessing**, **tokenization**, and **sequence generation**
- Training **loss and accuracy visualization**
- Example scripts for generating Urdu text from a seed phrase

## Project Structure

| File Name                          | Description                                            |
|------------------------------------|--------------------------------------------------------|
| `Text-Generation_Char-Level.ipynb` | Character-level Urdu text generation models            |
| `Text-Generation_Word-Level.ipynb` | Word-level Urdu text generation models                 |
| Urdu corpus files                  | Required for training and evaluation                   |

## Requirements

- Python 3.x
- TensorFlow 2.x
- Pandas
- NumPy
- Matplotlib
- KaggleHub (for dataset download)

Install dependencies using:

```bash
pip install tensorflow pandas numpy matplotlib kagglehub
```

## Usage

### 1. Prepare Data

- Download the Urdu corpus using KaggleHub (handled within the scripts).
- Ensure the corpus files are accessible at the specified paths.

### 2. Train a Model

- Run `Text-Generation_Char-Level.ipynb` for character-level generation.
- Run `Text-Generation_Word-Level.ipynb` for word-level generation.

Each script will:
- Load and preprocess the data
- Tokenize the text (character-level or word-level)
- Build and train the selected model (LSTM, GRU, or SimpleRNN)
- Plot training loss and accuracy

### 3. Generate Urdu Text

Use the provided `generate_text` function in each script:

```python
seed = "بس اتنی سی بات"
generated = generate_text(seed, next_chars=100, temperature=0.7)  # Character-level
# or
generated = generate_text(seed, next_words=6, temperature=0.7)    # Word-level
print(generated)
```

### 4. Example Output

The scripts print multiple text generations for a given Urdu seed phrase after training.

## Model Architectures

- **Embedding Layer:** Converts tokens to dense vectors
- **RNN Layer:** LSTM, GRU, or SimpleRNN for sequence modeling
- **Dense Layer:** Softmax output for next character/word prediction

## Visualization

Training loss and accuracy are plotted after each model is trained to help visualize learning progress.

## Customization

- Adjust sequence length (`seq_length`) for longer or shorter context
- Change model parameters (embedding size, RNN units, epochs)
- Use your own Urdu corpus by modifying the data loading section

## License

This project is provided for educational and research purposes.

