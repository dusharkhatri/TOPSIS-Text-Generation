# TOPSIS for Text Generation Models

## Overview
This project implements the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method to evaluate and rank pre-trained text generation models based on multiple performance metrics.

## Features
- Uses **TOPSIS** to rank text generation models.
- Evaluates models based on **Perplexity, BLEU Score, ROUGE Score, Execution Time, and Memory Usage**.
- Provides a normalized decision matrix for fair comparison.
- Outputs results to a CSV file for easy analysis.

## Dataset
The dataset consists of performance metrics for different text generation models, including:
- **GPT-3.5**
- **T5-Large**
- **BERT Fine-Tuned**

Each model is evaluated based on:
1. **Perplexity** (Lower is better)
2. **BLEU Score** (Higher is better)
3. **ROUGE Score** (Higher is better)
4. **Execution Time** (Lower is better)
5. **Memory Usage** (Lower is better)

## Installation
Ensure you have Python 3.7+ installed. Install the required libraries:
```bash
pip install numpy pandas
```

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/TOPSIS-Text-Generation.git
   cd TOPSIS-Text-Generation
   ```
2. Run the Python script:
   ```bash
   python topsis_text_generation.py
   ```
3. The results will be saved in `topsis_results.csv`.

## Output
The script generates a **ranked list** of models based on their performance. Example output:
```plaintext
TOPSIS Results saved to topsis_results.csv
```
The CSV file will contain:
| Model            | TOPSIS Score | Rank |
|------------------|-------------|------|
| GPT-3.5         | 0.87        | 1    |
| T5-Large        | 0.72        | 2    |
| BERT Fine-Tuned | 0.65        | 3    |

## Explanation of TOPSIS Method
1. **Normalization**: Convert all criteria into a comparable scale.
2. **Weighting**: Assign relative importance to each criterion.
3. **Ideal & Negative Ideal Solutions**: Identify best and worst possible values.
4. **Distance Calculation**: Compute distance from ideal and negative ideal points.
5. **Ranking**: Compute TOPSIS scores and rank models accordingly.

## License
This project is licensed under the **MIT License**.
