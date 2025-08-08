# AutoCorrect On Arabic-


# Arabic Text Autocorrection with BERT and Jaccard Similarity

link to notebook  https://colab.research.google.com/drive/1jkugwZGgIoq5LFahNs4OW3Af_iQ7NPcl?usp=sharing

This project implements an Arabic text autocorrection system using fine-tuned BERT models enhanced with Jaccard similarity for improved word comparison and correction.

## Overview

The system combines  powerful approache for text correction:

 **BERT-based Masked Language Modeling**: Uses a fine-tuned twitter/twhin-bert-large model to predict corrections for Arabic text based on context.

## Features

- **Accurate Arabic text correction** with context-aware BERT predictions
- **Enhanced with Jaccard similarity** for better handling of common misspellings
- **Interactive Gradio interface** 
  - Text correction with detailed correction information
- **Efficient processing** with chunking for long texts
- **Robust error handling** with fallback mechanisms

## Usage

### Online Demo

You can try the model directly in your browser using the Gradio interface.

### Local Installation

1. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

2. Extract the model files:
   ```
   unzip arabic_autocorrect_model.zip
   ```

3. Run the Gradio interface:
   ```python
   python run_arabic_autocorrect.py
   ```

## Model Information

- **Base model**: twitter/twhin-bert-large
- **Fine-tuned on**: Arabic text correction dataset with 30,574 pairs of incorrect/correct text
- **Training method**: Masked language modeling
- **Dictionary size**: Contains similarity mappings for 5,000 most common Arabic words

## Technical Details

### Correction Process

1. The text is tokenized into words
2. For each Arabic word:
   - First, the BERT model attempts to predict a correction based on context
3. Detailed correction information is provided, showing which method was used

### Performance

The model was evaluated on a test set of Arabic text pairs, measuring:
- BLEU score
- Character-level accuracy

## License

This project is provided for educational and research purposes.

## Acknowledgments

- Built using Hugging Face Transformers
- Interface created with Gradio
- Developed as part of the NTI Summer Program final project
