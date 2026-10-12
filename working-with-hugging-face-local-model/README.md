 <div align="center">

<h1>Working with Hugging Face Local Models</h1>

<p><strong>Learn how to download models from Hugging Face Hub, store them locally, and load them from a local directory.</strong></p>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Transformers](https://img.shields.io/badge/Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Jupyter Notebooks](https://img.shields.io/badge/Jupyter%20Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

This repository contains the tutorial notebook for downloading and loading machine learning models from Hugging Face Hub into a local directory.

## 1. Tutorial Details

[Working with Hugging Face Local Models](https://aviosit.com/tutorials/working-with-hugging-face-local-models) — Learn how to download a model repository, store its files locally, inspect the downloaded files, and load the model from a local directory using Transformers.

[Tutorial Video Demonstration](YOUTUBE_VIDEO_LINK_TUTORIAL) — Watch the tutorial walkthrough and follow the model downloading and loading process in practice.

The main tutorial notebook is available at [`notebook/working_with_hugging_face_local_models.ipynb`](notebook/working_with_hugging_face_local_models.ipynb).

The notebook uses `BAAI/bge-m3` as an example model. It downloads the model files using `huggingface_hub`, loads the tokenizer and model using Transformers, and verifies the model configuration.

## 2. Related Projects

`BAAI/bge-m3` is an example model used in AI applications, such as ChatQuran, for generating text embeddings.

[ChatQuran: A Multilingual RAG Application](https://aviosit.com/projects/chatquran) — Explore a multilingual Quranic question-answering application built using Retrieval-Augmented Generation (RAG).

[Project Video Demonstration](YOUTUBE_VIDEO_LINK_PROJECT) — Watch the project walkthrough and explore its implementation and development process.

[Live Demo](LIVE_DEMO_LINK) — Try the ChatQuran application and explore the project in practice.

## 3. Model Source

This tutorial uses the [`BAAI/bge-m3`](https://huggingface.co/BAAI/bge-m3) model from Hugging Face Hub.

The model files are downloaded to `models/bge-m3` at the repository root. The notebook uses this local directory to inspect the downloaded files and load the tokenizer and model.

The tutorial covers the following steps:

- **Model Repository** — Identify the model using its Hugging Face repository ID.
- **Model Download** — Download the model files to a local directory.
- **Local Storage** — Store the downloaded files in `models/bge-m3`.
- **Model Loading** — Load the tokenizer and model from the local directory using Transformers.
- **Verification** — Inspect the model configuration and hidden size to verify that loading was successful.

The initial download requires network access and sufficient disk space. Once the required files are available locally, the model can be loaded with `local_files_only=True` to prevent Transformers from downloading missing files from Hugging Face Hub during loading.

> **Important:** Model files are excluded from Git to avoid committing large binary files. Run the notebook to download the model locally before loading it. The local model files are not included in this repository.

## 4. Requirements

Make sure you have the following installed:

- [Python](https://www.python.org/) 3.13
- [uv](https://docs.astral.sh/uv/)
- [Jupyter](https://jupyter.org/) or a Jupyter-compatible environment

The tutorial uses the following Python packages:

- `huggingface-hub` — `2.2.0`
- `transformers` — `5.19.0`
- `torch` — `2.14.1`
- `ipykernel` — `7.4.0` (development dependency)

These versions reflect the environment resolved by `uv` for this repository. The project dependencies are managed using `uv` and recorded in [`pyproject.toml`](../pyproject.toml) and [`uv.lock`](../uv.lock).

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

- Open [`notebook/working_with_hugging_face_local_models.ipynb`](notebook/working_with_hugging_face_local_models.ipynb) in VS Code or another compatible Jupyter environment.

- Select the `aviosit-tutorials` kernel.

- Run the notebook cells in order, starting with the model path configuration section.

The notebook downloads `BAAI/bge-m3` into `models/bge-m3` at the repository root. If the required model files are already present, the notebook skips the download step. Otherwise, `snapshot_download()` retrieves the model files that are missing. Ensure that network access is available for the initial download and that sufficient disk space is available for the model files.

## 6. Expected Outcome

By completing this tutorial, you will have:
- downloaded a model from Hugging Face Hub,
- stored its files locally, and
- loaded the tokenizer and model from the local directory. 

You will also understand how to organise local model files and verify that a model has loaded correctly. This tutorial focuses on model downloading and loading only. Embedding generation is covered in the next tutorial: [How to Embed Texts for AI Applications](https://aviosit.com/tutorials/embedding-texts-for-ai-applications).

---

<div align="center">

<!-- TUTORIAL LINKS -->

<a href="https://aviosit.com/tutorials/working-with-hugging-face-local-models">
  <img src="https://img.shields.io/badge/🌐%20Web%20Page-2563EB?style=for-the-badge" alt="Web Page">
</a>
<a href="YOUTUBE_VIDEO_LINK_TUTORIAL">
  <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
</a>

</div>