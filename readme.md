# IACR 2025 LLM Workshop

Welcome to the online materials of the pre-conference LLM workshop for the International Association of Cancer Registries 2025 in Izmir, Turkey (https://www.iacr2025.com/pre-conference-workshop) written by [Dimitris Katsimpokis](https://www.linkedin.com/in/dkatsimpokis/) and [Irene Cara](https://www.linkedin.com/in/irene-cara/). The workshop features hands-on sessions on text classification and Retrieval-Augmented Generation (RAG).

## Workshop Overview

The workshop consists of two main sessions designed to provide practical experience with modern LLM techniques in healthcare and research contexts.

| Session  | Notebook  |
|---|---|
| Session 1: Text classification  | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/IKNL/iacr_2025_llm_workshop/blob/main/notebooks/text_classification/IACR_text_classification.ipynb)  |
| Session 2: Retrieval-Augmented Generation (RAG) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/IKNL/iacr_2025_llm_workshop/blob/main/notebooks/retrieval_augmented_generation/RAG.ipynb)   |

## Repository Structure

```
├── data/                           # Workshop datasets
├── model/                          # Model files and configurations
├── notebooks/                      # Jupyter notebooks for workshop sessions
│   ├── retrieval_augmented_generation/
│   │   ├── RAG.ipynb               # Main RAG workshop notebook
│   │   └── helper_notebooks/       # Helper notebooks (i.e., data parsing)
│   └── text_classification/
│       └── IACR_text_classification.ipynb # Text classification workshop
├── requirements.txt                 # Python dependencies
├── LICENSE.md                       # MIT License
└── readme.md                        # This file
```

### Running the Notebooks

#### Option 1: Google Colab (Recommended)
Click the "Open in Colab" badges above to run the notebooks in Google Colab with pre-configured environments.

#### Option 2: Local Jupyter
```bash
jupyter notebook notebooks/
```

## Session Details

### Session 1: Text Classification
Learn how to implement and fine-tune LLMs for text classification tasks using healthcare data. The session covers:
- TF-IDF vectorization for turning text into a numerical representation
- Not fine-tuned sentence embedding model to get contextual embeddings, in combination with a random forest classifier
- Few-shot finetuning sentence embedding models with Setfit
- Zero-shot classification with the HugginFace pipeline
- Evaluation of all previous models on WHO performance status classification

### Session 2: Retrieval-Augmented Generation (RAG)
Explore RAG techniques for enhancing LLM responses with external knowledge. Topics include:
- Document embedding and vector databases
- Retrieval mechanisms and similarity search
- Context integration and prompt engineering
- Evaluation of RAG on Adverse Events and Cancer in 5 Continents data

## Data Sources

The workshop utilizes:
- **Fake clinical note data** ([data/IACR_PS_workshop.csv](data/IACR_PS_workshop.csv))
- **CTCAE v4 data** - Common Terminology Criteria for Adverse Events (https://evs.nci.nih.gov/ftp1/CTCAE/CTCAE_4.03/Archive/CTCAE_4.0_2009-05-29_QuickReference_8.5x11.pdf)
- **Cancer Incidence in 5 Continents (CI5) v12** - Cancer Incidence data from all over the world (https://ci5.iarc.fr/ci5-xii/)


## For local installation only (Option 2 above)

1. Clone the repository:
```bash
git clone https://github.com/IKNL/iacr_2025_llm_workshop.git
cd iacr_2025_llm_workshop
```

2. Create a virtual environment:
```bash
python -m venv workshop-env
source workshop-env/bin/activate  # On Windows: workshop-env\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contributors

Developed by Dimitris Katsimpokis (d.katsimpokis@iknl.nl) and Irene Cara (i.cara@iknl.nl) working at the Netherlands Comprehensive Cancer Organisation (Integraal Kankercentrum Nederland; IKNL)


## Support


For questions or issues during the workshop, please raise an issue in this repository or contact the workshop organizers.
