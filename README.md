# LLM Fundamentals

A lightweight, hands-on project to learn and experiment with the foundational concepts required to work with Large Language Models (LLMs). It uses PyTorch and Hugging Face Transformers to explore tokenization, embeddings, and practical workflows for running and inspecting models.

## Contents
- Tokenization fundamentals: subword tokenization (WordPiece/BPE), special tokens, mapping between tokens and IDs, and how IDs map to embeddings.
- Simple embedding explorations and analogies using pre-trained models (e.g., DistilBERT).

## Project Structure
- `tokenization.ipynb`: Main notebook covering tokenization concepts and basic embedding lookups.
- `requirements.txt`: Python dependencies required to run the notebooks.

## Requirements
- Python 3.11 (see `requirements.txt` for package versions)
- Recommended: a virtual environment (venv or conda)
- CPU is sufficient for these notebooks; a GPU is optional

## Quickstart
### 1) Create and activate a virtual environment (Windows PowerShell)
```powershell
python -m venv .venv
. .venv\Scripts\Activate.ps1
```

On macOS/Linux:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2) Install dependencies
```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

If you prefer a CPU-only PyTorch wheel (often faster to install on Windows):
```bash
python -m pip install torch==2.6.0 --index-url https://download.pytorch.org/whl/cpu
```

### 3) Launch Jupyter
```bash
python -m jupyter lab
```
Or:
```bash
python -m jupyter notebook
```

## Usage
1. Open `tokenization.ipynb` in Jupyter Lab/Notebook.
2. Run the cells sequentially. The notebook will download any required pre-trained weights and tokenizer files on first run (cached under your user profile by Hugging Face).
3. Modify the examples to explore token IDs, embeddings, and tokenization edge cases.

## Troubleshooting
- Token not found in vocabulary: some strings may map to the unknown token. Try lowercasing or inspecting the tokenizer with `tokenizer.tokenize(text)`.
- Slow installs on Windows: consider the CPU-only PyTorch wheel shown above.
- PowerShell policy errors: run Jupyter via `python -m jupyter lab` instead of a global shim, or adjust execution policies according to your IT constraints.

## Contributing
- Issues and pull requests are welcome. Please keep notebooks clean (clear outputs before committing, or use tools like `nbstripout`).
- Follow a conventional commit style for messages (e.g., `feat:`, `fix:`, `chore:`) when possible.

## License
Specify your project license here (e.g., MIT). If no license is provided, all rights are reserved by default.

## Acknowledgments
- [PyTorch](https://pytorch.org)
- [Hugging Face Transformers](https://huggingface.co/transformers)
