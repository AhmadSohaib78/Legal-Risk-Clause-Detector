# Legal Risk Clause Detector

This project is an AI-powered tool designed to automatically detect and flag potentially risky clauses within legal contracts. By leveraging state-of-the-art sentence embeddings and semantic similarity techniques, it assists legal teams in identifying risk-prone language during contract review.

## Project Overview

The system extracts clauses from uploaded contracts, encodes them using Sentence-BERT (all-MiniLM-L6-v2), and compares each clause to a predefined set of known risky patterns or to a universal similarity threshold. Clauses with high semantic similarity are flagged as potentially risky.

## Features

- Accepts contracts in PDF format.
- Extracts clauses from contracts.
- Uses a pre-trained transformer model for sentence embeddings.
- Performs similarity analysis using cosine similarity.
- Supports both rule-based and AI-based clause evaluation.
- Generates audit logs for traceability and review.

## Modules

| Module | Description |
|--------|-------------|
| Module 6 | Extract clauses from uploaded contracts. |
| Module 7 | Perform AI-based universal risk detection using sentence embeddings. |
| Module 8 | Apply rule-based detection against predefined risky clauses. |

## Technical Details

- **Model Used**: Sentence-BERT (all-MiniLM-L6-v2)
- **Embedding Size**: 384 dimensions per clause
- **Similarity Metric**: Cosine similarity
- **Language**: Python
- **Libraries**: `transformers`, `sentence-transformers`, `PyMuPDF`, `scikit-learn`, `NumPy`

## Example Risky Clauses

- "The service provider shall not be liable for any loss or damage..."
- "This agreement may be terminated at any time by either party..."
- "No warranties, express or implied, are provided..."

## Output

- Prints and/or stores a list of risky clauses.
- Provides a similarity score and matched pattern for each flagged clause.
- Optionally logs all analysis steps for audit purposes.

## Setup and Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Legal-Risk-Clause-Detector.git
   cd Legal-Risk-Clause-Detector
