<div align="center">

<h1>Preparing Quran Data for a RAG System</h1>

<p><strong>An exploration of Quran corpus data and the data preparation process for retrieval-augmented generation (RAG).</strong></p>

![TXT File](https://img.shields.io/badge/%F0%9F%93%84%20txt%20file-412991?style=for-the-badge&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Parquet](https://img.shields.io/badge/parquet-50ABF1?style=for-the-badge&logo=apacheparquet&logoColor=white)
![Jupyter Notebooks](https://img.shields.io/badge/Jupyter%20Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

This repository contains the exploratory notebook for preparing Quran source data for use in a retrieval-augmented generation (RAG) system.

## 1. Tutorial Details

[Preparing Quran Data for a RAG System](https://aviosit.com/tutorials/preparing-quran-data-for-rag) — Explore the detailed tutorial, concepts, data preparation process, and implementation notes.

[Tutorial Video Demonstration](YOUTUBE_VIDEO_LINK_TUTORIAL) — Watch the tutorial walkthrough and follow the Quran data preparation process in practice.

The main tutorial notebook is available at [`notebooks/preparing_quran_dataset.ipynb`](notebooks/preparing_quran_dataset.ipynb).

The notebook explores the raw Quran sources, validates their structure, combines the Arabic and translation data, and prepares the resulting dataset as Parquet.

## 2. Related Projects

[ChatQuran: A Multilingual Quran RAG Application](https://aviosit.com/projects/chatquran) — Explore the complete ChatQuran project and its RAG development roadmap.

[Project Video Demonstration](YOUTUBE_VIDEO_LINK_PROJECT) — Watch the ChatQuran project walkthrough and explore its implementation and development process.

[Live Demo](LIVE_DEMO_LINK) — Try the ChatQuran application and explore the project in practice.

## 3. Data Sources

The tutorial uses Quran sources provided through [Tanzil](https://tanzil.net/):

- **Arabic Quran** text: [Tanzil Quran Text](https://tanzil.net/download/)
- **English** translation: [Tanzil Translation](https://tanzil.net/trans/) — Saheeh International
- **Indonesian** translation: [Tanzil Translation](https://tanzil.net/trans/) — Bahasa Indonesia, Indonesian Ministry of Religious Affairs

See the [Tanzil Text License](https://tanzil.net/docs/Text_License) and the applicable translation terms before redistributing or using the source data outside this tutorial.

The source data is kept locally under `data/raw/` and is not committed to this repository.

## 4. Requirements

Make sure you have the following installed:

- [Python](https://www.python.org/) 3.13
- [uv](https://docs.astral.sh/uv/) 0.12.17
- [Jupyter](https://jupyter.org/) or a Jupyter-compatible environment

The tutorial depends on:

- `pandas >= 2.3.3`
- `PyArrow >= 21.0.0`
- `ipykernel >= 6.31.0`

## 5. How to Run

### A. Installation

Clone the repository:

```bash
git clone https://github.com/mj-muhajirin/aviosit-tutorials
```

Go to the repository:

```bash
cd aviosit-tutorials
```

Install the project dependencies:

```bash
uv sync
```

Install the Jupyter kernel if it has not already been installed:

```bash
uv run python -m ipykernel install --user --name aviosit-tutorials --display-name "Python (AviosIT Tutorials)"
```

### B. Run the Tutorial

Open `preparing-quran-data-for-rag/notebooks/preparing_quran_dataset.ipynb` in VS Code or another compatible Jupyter environment.

Select the `aviosit-tutorials` kernel.

The notebook expects the Quran source files under `preparing-quran-data-for-rag/data/raw/`.

The prepared dataset is generated at `preparing-quran-data-for-rag/data/processed/quran.parquet`.

The raw source files and generated dataset are intentionally excluded from Git.

## 6. License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">

<!-- TUTORIAL LINKS -->

<a href="https://aviosit.com/tutorials/preparing-quran-data-for-rag">
  <img src="https://img.shields.io/badge/🌐%20Web%20Page-2563EB?style=for-the-badge" alt="Web Page">
</a>
<a href="https://www.youtube.com/playlist?list=PLYZCMegpMb8E">
  <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
</a>

</div>