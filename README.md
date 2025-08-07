# HyP-KGRAG: Hypothetical Path-Based Knowledge Graph Retrieval Augmented Generation with DeepSeek

This repository contains all code, data, and prompt templates used in my work on Knowledge Graph Question Answering (KGQA), based on the DeepSeek V3 model. The proposed **HyP-KGRA** framework enhances QA by generating hypothetical triples, aligning them in vector space, and refining them through denoising and reranking.
![HyP-KGRAG](https://github.com/user-attachments/assets/eb7fcbe0-5549-404c-aa90-78fb8f410241)

---

## 📁 Repository Structure

### 🔹 `Data`

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

### 📒 `Notebook`

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

### 🧠 `Prompt`

This folder includes all prompt templates used in each notebook. Every script in this project is built on top of the **DeepSeek V3** language model. Prompt files are named to match the corresponding notebooks for easy reference and reproducibility.

---

## 🚀 Getting Started

下面是更新后的 **Getting Started** 部分，用英文重写并整合你给出的说明，使其清晰、简洁且专业：

---

## 🚀 Getting Started

1. **Install all dependencies**
   It is strongly recommended to use a virtual environment (e.g., `conda` or `venv`) before installing the required packages:

   ```bash
   pip install -r requirements.txt
   ```

2. **Run the notebooks in the following order:**

   > 🔁 *Start with data preprocessing → then run retrieval & query rewriting → finally execute the main framework.*

   * **Step 1: Preprocess the Knowledge Graph**

     * `KGPreprocess.ipynb`

   * **Step 2: Run Retriever and Rewriter (choose one baseline):**

     * Retrieval:

       * `BGE-M3_Retriever.ipynb` *or* `BM25_Retriever.ipynb`
     * Query Rewriting:

       * `BGE-M3_Retwriter.ipynb` *or* `BM25_Rewriter.ipynb`

   * **Step 3: Run the Main Framework**

     * `HyPKGRAG.ipynb`

---
## 🧪 Notes

* The core idea of this project is the **HyP-KGRA** framework, which introduces hypothetical triples based on reasoning paths and aligns them with factual triples in a shared vector space.
* All code has been tested locally. If using your own data, please adjust file paths and formats accordingly.
