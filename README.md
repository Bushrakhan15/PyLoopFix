# PyLoopFix: Pattern-Guided Automated Program Repair for Python Loop Performance Bugs

This repository contains the implementation and experimental artifacts for a research study on automatically
repairing slow loops in Python programs.

## Repository Structure

```
PyLoopFix/
├── pyloopfix/        # PyLoopFix notebooks (DeepSeek and GPT versions)
├── baselines/
│   ├── fasterpy/     # FasterPy baseline
│   ├── prompting/    # Simple prompting baselines (with / without feedback)
│   ├── sbllm/        # SBLLM baseline
│   └── single_llm/   # Single-LLM baselines
├── data/             # Pattern knowledge base, test cases, benchmark loops
└── results/          # Output files from all runs
```

## Data

| File | What it is |
|------|------------|
| `data/pattern_knowledge_base.json` | Loop optimization patterns used by PyLoopFix |
| `data/test_loop_filtered_verified.jsonl` | Benchmark loops used for evaluation |
| `data/test_cases.zip` | Test cases for checking correctness |
| `data/kb_loop_filtered.zip` | Filtered loop examples for the knowledge base |
| `data/kb_summaries_checkpoint.zip` | Saved pattern summaries |

## How to Run

1. Unzip the files in `data/`.
2. Open a notebook in `pyloopfix/` or `baselines/` (Jupyter or Google Colab).
3. Add your API key (OpenAI or DeepSeek) in the first cell.
4. Run all cells. Results are saved to `results/`.

## Requirements

- Python 3.x
- Jupyter Notebook
- OpenAI / DeepSeek API access
