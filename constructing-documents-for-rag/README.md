<div align="center">

<h1>Constructing Documents for RAG Applications</h1>

<p><strong>Learn how to transform a structured Quran dataset into documents with text and metadata for Retrieval-Augmented Generation (RAG) applications.</strong></p>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Parquet](https://img.shields.io/badge/Apache%20Parquet-50ABF1?style=for-the-badge&logo=apacheparquet&logoColor=white)
![Jupyter Notebooks](https://img.shields.io/badge/Jupyter%20Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

This repository contains the tutorial notebook for constructing documents from a prepared Quran dataset for use in a Retrieval-Augmented Generation (RAG) application.

## 1. Tutorial Details

[How to Construct Documents for RAG Applications](https://aviosit.com/tutorials/constructing-documents-for-rag) — Learn how to transform a structured Quran dataset into documents containing text and metadata for subsequent embedding, indexing, and retrieval in a RAG pipeline.

[Tutorial Video Demonstration](PLACEHOLDER) — Watch the tutorial walkthrough and follow the document construction process in practice.

The main tutorial notebook is available at [`notebooks/constructing_documents_for_rag.ipynb`](notebooks/constructing_documents_for_rag.ipynb).

The notebook loads a prepared Quran dataset, constructs documents from individual ayah records in multiple languages, and organises each document into an ID, text, and metadata. It then validates and inspects the resulting documents.

## 2. Related Projects

[ChatQuran: A Multilingual Quran RAG Application](https://aviosit.com/projects/chatquran) — Explore the ChatQuran project, which applies Retrieval-Augmented Generation to multilingual Quranic question answering.

[Project Video Demonstration](YOUTUBE_VIDEO_LINK_PROJECT) — Watch the ChatQuran project walkthrough and explore its implementation and development process.

[Live Demo](LIVE_DEMO_LINK) — Try the ChatQuran application and explore the project in practice.

## 3. Data Sources

This tutorial uses a prepared Quran dataset produced by the preceding [Preparing Quran Dataset for RAG Applications](https://aviosit.com/tutorials/preparing-quran-dataset-for-rag) tutorial.

The dataset is expected to contain the following columns:

- `surah`
- `ayah`
- `arabic`
- `english`
- `indonesian`

The notebook transforms each ayah record into separate language-specific documents. Each document contains:

- **ID** — a unique identifier for the document.
- **Text** — the text content used in subsequent retrieval stages.
- **Metadata** — structured information that identifies the source ayah and language.

The prepared dataset is read from `data/processed/quran.parquet`. A synthetic example dataset is also provided at `data/processed/quran-example.parquet` so that readers can follow the tutorial without requiring the full dataset.

**Important:** The example dataset contains synthetic placeholder text for demonstration only. It does not contain actual Quranic text or translations.

The full processed dataset is excluded from Git. Readers can use the example dataset provided in this repository or replace the dataset path with their own locally available dataset.

## 4. Requirements

Make sure you have the following installed:

- [Python](https://www.python.org/) 3.13
- [uv](https://docs.astral.sh/uv/) 0.12.17
- [Jupyter](https://jupyter.org/) or a Jupyter-compatible environment

The tutorial uses the following Python packages:

- `pandas >= 2.3.3`
- `PyArrow >= 21.0.0`
- `ipykernel >= 6.31.0`

The project dependencies are managed using `uv` and declared in the repository's `pyproject.toml` and `uv.lock` files.

## 5. How to Run

### A. Installation

Clone the repository:

```bash
git clone https://github.com/mj-muhajirin/aviosit-tutorials.git
```

Navigate to the repository directory:

```bash
cd aviosit-tutorials
```

Install the project dependencies:

```bash
uv sync
```

Register the Jupyter kernel if it has not already been installed:

```bash
uv run python -m ipykernel install --user --name aviosit-tutorials --display-name "Python (AviosIT Tutorials)"
```

### B. Run the Tutorial

Open `notebooks/constructing_documents_for_rag.ipynb` in VS Code or another compatible Jupyter environment.

Select the `aviosit-tutorials` kernel.

Run the notebook cells in order, starting with the dataset-loading section.

The notebook supports loading the prepared dataset from either the repository root or the notebook directory, using the corresponding relative path.

By default, use the included `quran-example.parquet` dataset to follow the tutorial. If you want to use the full dataset, make sure `quran.parquet` is available locally and update the dataset path in the notebook accordingly.

The full dataset is excluded from Git and must be prepared separately using the [Preparing Quran Dataset for RAG Applications](https://aviosit.com/tutorials/preparing-quran-dataset-for-rag) tutorial or supplied from another local source.

## 6. Expected Outcome

By completing this tutorial, you will have constructed a collection of language-specific documents from a structured Quran dataset.

Each document contains an ID, text, and metadata that preserve its relationship to the original ayah and language. These documents provide the input representation for subsequent RAG stages, including embedding, indexing, and retrieval.

This tutorial focuses on document construction. Embedding generation, vector indexing, retrieval, and answer generation are covered in subsequent stages of the ChatQuran project.

---

<div align="center">

<!-- TUTORIAL LINKS -->

<a href="https://aviosit.com/tutorials/constructing-documents-for-rag">
  <img src="https://img.shields.io/badge/🌐%20Web%20Page-2563EB?style=for-the-badge" alt="Web Page">
</a>
<a href="https://www.youtube.com/watch?v=LHXr8NMTM4E">
  <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
</a>

</div>