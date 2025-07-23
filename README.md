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

| Module     | Description |
|------------|-------------|
| Module 1   | Initialize UI and necessary configurations. |
| Module 2   | Load uploaded contract file (PDF). |
| Module 3   | Extract text content from the PDF. |
| Module 4   | Preprocess and segment text into individual clauses. |
| Module 5   | Load Sentence-BERT model (all-MiniLM-L6-v2) for embeddings. |
| Module 6   | Generate embeddings for each clause in the contract. |
| Module 7   | Compare embeddings with a universal threshold for risk detection. |
| Module 8   | Rule-based matching with known risky clause patterns. |
| Module 9   | Log and display flagged clauses along with similarity scores. |
| Module 10  | Optional enhancements such as filtering, exporting results, or UI styling. |

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

- Displays a list of risky clauses from the uploaded document.
- Provides similarity scores and matched pattern details.
- Supports logging for review and audit trails.
