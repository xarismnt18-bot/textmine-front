# TopicMiner

**A free, browser-based NLP platform for comparative topic modelling and sentiment analysis with AI-assisted interpretation.**

🔗 **Live platform:** [xarismnt18-bot.github.io/TopicMiner](https://xarismnt18-bot.github.io/TopicMiner)  
📦 **Zenodo archive:** [10.5281/zenodo.19324564](https://doi.org/10.5281/zenodo.19324564)

---

## Overview

TopicMiner is a research-grade, browser-based NLP platform that requires no programming expertise or software installation. It integrates five analysis methods in a single unified interface:

- **LDA** (Latent Dirichlet Allocation) topic modelling
- **BERTopic** neural topic modelling
- **TF-IDF** keyword extraction
- **Word Cloud** visualisation
- **Dual-model Sentiment Analysis** (VADER and RoBERTa)

A distinguishing feature is its **AI-assisted interpretation layer**, powered by the Claude API (Anthropic), which provides corpus summaries, domain-specific stopword suggestions, and an interactive evaluation chat to help users interpret results without requiring methodological expertise.

---

## Features

- Upload TXT, PDF, or XLSX files via drag-and-drop
- Coherence-based optimal K selection for LDA (C_V metric via Gensim)
- Comparative sentiment analysis: VADER vs. RoBERTa side by side
- AI corpus summary and stopword advisor after every analysis run
- Interactive AI evaluation chat for natural language result interrogation
- Export results as formatted PDF reports (client-side, via jsPDF)
- No installation, no account required — runs entirely in the browser

---

## Architecture

| Component | Technology |
|---|---|
| Frontend | HTML / CSS / JavaScript, hosted on GitHub Pages |
| Primary backend | FastAPI (Python 3.11), deployed on Render |
| GPU backend | Google Colab + ngrok (BERTopic, RoBERTa) |
| AI layer | Anthropic Claude API |
| Coherence scoring | Gensim 4.3 (C_V metric) |
| Topic modelling | scikit-learn (LDA), BERTopic |
| Sentiment analysis | VADER, Cardiff NLP RoBERTa |

---

## Notes

BERTopic and RoBERTa analyses rely on an optional GPU-enabled backend hosted through Google Colab and ngrok.

When the Colab notebook is not running, the platform may display the status "Unreachable". This is expected behaviour and only affects transformer-based analyses.

All other functionalities (LDA, TF-IDF, WordCloud, Coherence Evaluation and VADER Sentiment Analysis) remain fully operational.

## Citation

If you use TopicMiner in your research, please cite:

```
Mentsios CN (2026). TopicMiner: An Accessible Web Platform for Comparative 
Topic Modelling and Sentiment Analysis with AI-Assisted Interpretation (v1.0.0). 
Zenodo. https://doi.org/10.5281/zenodo.19324564
```

---

## Authors

- **Charalampos Nikolaou Mentsios** — Department of Electrical and Electronics Engineering, University of West Attica, Athens, Greece

---

## License

This project is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
