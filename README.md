# 🗣️ Dialect Word Mining in Turkish Speaking

This repository accompanies the final submission for the **COS7045-B Advanced Machine Learning** module. It focuses on identifying and analyzing dialect-specific vocabulary from spoken Turkish, Kurmancî (Kurdish), and Zazakî using automatic speech recognition (ASR), word mining, and graph-based knowledge representation.

## Project Overview

This project aims to:
- Transcribe speech data using pretrained and fine-tuned ASR models
- Extract and analyze frequent words across dialects
- Visualize vocabulary overlaps and distinctions
- Construct a frequency-based knowledge graph showing word co-occurrence relationships

The pipeline supports future research in dialect-aware AI and helps preserve underrepresented languages in digital NLP systems.

## Technologies Used

- Hugging Face Transformers (Whisper, Wav2Vec2)
- Mozilla Common Voice datasets (Turkish, Kurmancî, Zazaki)
- NetworkX for knowledge graph construction
- Matplotlib for visualization
- Pandas & JiWER for evaluation and WER scoring

## Project Structure

```plaintext
dialectalwordmining/
├── notebooks/                # All project notebooks
│   ├── turkish_*.ipynb
│   ├── kurmanci_*.ipynb
│   ├── zazaki_*.ipynb
│   ├── download_models.ipynb
│   ├── construct_knowledge_graph.ipynb
│   └── visualize_dialectal_graph.ipynb
│
├── data/                     # Cleaned TSVs only (clips excluded)
│   └── [language]/dev.tsv
│
├── outputs/
│   ├── transcriptions/       # ASR outputs and unmatched .csvs
│   ├── frequencies/          # Word frequency tables per dialect
│   ├── visualizations/       # Plots + co-occurrence .gexf files
│   └── knowledge_graph/      # Final combined knowledge graph
│
├── models/                   # (optional, not uploaded due to size)
├── requirements.txt
├── .gitattributes
├── .gitignore
├── README.md
└── COS7045B_dialect_word_mining_report.pdf
