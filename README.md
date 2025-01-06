# Multilingual Political Text Classification

This repository provides an implementation of text classification models for identifying political affiliations based on English and Turkish texts. Two approaches are utilized: a Masked Model leveraging multilingual BERT and a Causal Model leveraging Llama-3.2-1B.

## Masked Model

### Description
The Masked Model uses multilingual BERT for fine-tuning and classification:

- **English Text (Orientation Data):**
  - **Objective:** Predict whether sentences are authored by politically right-leaning or left-leaning individuals.
  - **Approach:** Fine-tune multilingual BERT with English text data.

- **Turkish Text (Power Data):**
  - **Objective:** Predict whether sentences are authored by ruling party-affiliated or opposition party-affiliated individuals.
  - **Approach:** Fine-tune multilingual BERT with Turkish text data.

### Implementation
1. **Data Preparation:**
   - Collect and preprocess English and Turkish datasets.
   - Label data according to political affiliation.
2. **Fine-Tuning:**
   - Use multilingual BERT for fine-tuning on labeled datasets.
3. **Inference:**
   - Predict political affiliation for new input texts.

## Causal Model

### Description
The Causal Model employs the Llama-3.2-1B model in a zero-shot classification manner for both English and Turkish texts:

- **Objective:** Classify text based on political affiliation without requiring fine-tuning.
- **Tasks:**
  - Classify English text for right/left political orientation.
  - Classify Turkish text for ruling/opposition party affiliation.
