# Custom Chatbot Project

A Retrieval-Augmented Generation (RAG) chatbot built with OpenAI embeddings and GPT-3.5-Turbo. This project demonstrates how providing domain-specific context through semantic search improves LLM answers compared to a base model with no context.

## Overview

The chatbot uses the **2023 Fashion Trends** dataset to answer questions about specific fashion trends. It works by:

1. **Embedding** each text entry using OpenAI's `text-embedding-ada-002` model
2. **Searching** for the most relevant entries via cosine similarity against the user's query
3. **Constructing a prompt** with retrieved context and sending it to GPT-3.5-Turbo
4. **Comparing** the custom RAG answer against a basic (no-context) answer to demonstrate the improvement

## Dataset

`data/2023_fashion_trends.csv` — 93 rows of fashion trend descriptions with source attributions, covering topics like denim styles, color palettes, and seasonal trends for Spring 2023.

## Project Structure

```
├── project.ipynb          # Main notebook with all implementation
├── data/
│   ├── 2023_fashion_trends.csv
│   ├── character_descriptions.csv
│   └── nyc_food_scrap_drop_off_sites.csv
├── INSTRUCTIONS.md        # Project instructions
├── RUBRIC.md              # Grading rubric
└── README.md
```

## Setup

1. Install dependencies:
   ```bash
   pip install openai pandas numpy tiktoken
   ```

2. Open `project.ipynb` and set your OpenAI API key in the client initialization cell.

3. Run all cells top to bottom.

## Requirements

- Python 3.9+
- openai
- pandas
- numpy
- tiktoken

## Acknowledgements

This project was built with assistance from [Claude Code](https://claude.ai/claude-code), Anthropic's CLI tool for AI-assisted software development.
