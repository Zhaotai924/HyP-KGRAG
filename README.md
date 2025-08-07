# HyP-KGRAG: Hypothetical Path-Based Knowledge Graph Retrieval Augmented Generation with DeepSeek

![HyP-KGRAG](https://github.com/user-attachments/assets/64257e87-367f-4457-af1e-e5b0a0c12485)


## 📁 Repository Structure

### 🔹 `Data/`

This folder contains all datasets and intermediate results used throughout the project. Each subfolder serves a specific purpose:

| Subfolder Name   | Description                                      |
| ---------------- | ------------------------------------------------ |
| `KGQA_Dataset/`  | Original datasets used for KGQA                  |
| `KG_Preprocess/` | Preprocessed data from the knowledge graph       |
| `BGEM3/`         | Intermediate data for the BGE-M3 baseline model  |
| `BM25/`          | Intermediate data for the BM25 baseline model    |
| `HyP-KGRA/`      | Process data for the proposed HyP-KGRA framework |
| `AblationTest1/` | Experimental data for ablation test 1            |
| `AblationTest2/` | Experimental data for ablation test 2            |

---

### 📒 `notebook/`

This folder includes all implementation code written in Jupyter Notebook. Each notebook corresponds to a component or experiment:

| Notebook                       | Purpose                                                                                                                                                                                                                                                                                                                 |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `HyPKGRAG.ipynb`               | ⭐ Main framework implementation, including: <br> - Generating Hypothetical Triples Through Reasoning Paths<br> - Constructing an Offline Vector Database for Embedded Triples<br> - Online Alignment of Hypothetical and Factual Triplets in Vector Space<br> - Denoising and Reranking<br> - Generation and Evaluation |
| `BGE-M3_Retriever.ipynb`       | BGE-M3-based knowledge retriever                                                                                                                                                                                                                                                                                        |
| `BM25_Retriever.ipynb`         | BM25-based knowledge retriever                                                                                                                                                                                                                                                                                          |
| `BGE-M3_Retwriter.ipynb`       | Query rewriting using BGE-M3 to enhance lexical and semantic match                                                                                                                                                                                                                                                      |
| `BM25_Rewriter.ipynb`          | Query rewriting using BM25 for lexical match enhancement                                                                                                                                                                                                                                                                |
| `Ablation_Verbalization.ipynb` | Used for analysis and visualization in ablation studies                                                                                                                                                                                                                                                                 |
| `KGPreprocess.ipynb`           | Preprocessing scripts for knowledge graph data                                                                                                                                                                                                                                                                          |

---

### 🧠 `Prompt/`

This folder includes all prompt templates used in each notebook. Every script in this project is built on top of the **DeepSeek V3** language model. Prompt files are named to match the corresponding notebooks for easy reference and reproducibility.

---

## 🚀 Getting Started

1. Install all dependencies (recommended to use a virtual environment or Conda).
2. Follow the suggested order to run notebooks:

   * `KGPreprocess.ipynb`
   * Retriever and Rewriter (choose one baseline):

     * `BGE-M3_Retriever.ipynb` / `BM25_Retriever.ipynb`
     * `BGE-M3_Retwriter.ipynb` / `BM25_Rewriter.ipynb`
   * Main framework:

     * `HyPKGRAG.ipynb`
   * Analysis and visualization:

     * `Ablation_Verbalization.ipynb`

---

## 🧪 Notes

* The core idea of this project is the **HyP-KGRA** framework, which introduces hypothetical triples based on reasoning paths and aligns them with factual triples in a shared vector space.
* All code has been tested locally. If using your own data, please adjust file paths and formats accordingly.

---

## 📬 Contact

If you have any questions or suggestions, feel free to open an issue on GitHub.

---

Would you like me to generate this as a downloadable `README.md` file for your repo?
