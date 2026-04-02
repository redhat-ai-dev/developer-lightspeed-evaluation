# Developer Lightspeed Evaluation

This branch contains the evaluation resources for **Developer Lightspeed 1.8**, including the source RAG documentation, the generated datasets, and the performance results across multiple LLMs.

## 📂 Repository Structure

| Path | Description |
| :--- | :--- |
| **[📂 rhdh-product-docs](./rhdh-product-docs-1.8-Nov19-2025)** | The Red Hat Developer Hub (RHDH) product documentation (v1.8) used as the source knowledge base for this evaluation. |
| **[📂 dataset](./dataset)** | Contains raw and processed Q&A pairs, formatted specifically for the `lightspeed-evaluation` tool. |
| **[📂 evaluation-result](./evaluation-result)** | Detailed metrics and outcome reports from the model evaluations. |
| **[📄 categories_rhdh.yaml](categories_rhdh.yaml)** | Manually defined topic groups used to classify and organize the Q&A pairs. |

---

## 🧪 Evaluation Overview

For the Developer Lightspeed 1.8 release, we ran evaluation against five distinct models.

**Models Evaluated:**
* **Gemini:** `gemini-2.5-pro`, `gemini-2.5-flash-lite`
* **GPT:** `gpt-oss-120b`
* **Llama:** `llama3.1:8b`, `llama4:scout`

**Judge Model being used:** `gemini-2.5-pro`

> 📊 **View Results:** For a deep dive into the performance metrics, please refer to the **[Evaluation Results](./evaluation-result)** directory.

---

## ⚙️ Methodology & Generation

The dataset in this repository was constructed using a synthetic generation pipeline to ensure comprehensive coverage of the documentation.

* **Source Material:** The dataset is derived entirely from the [RHDH 1.8 Product Docs](./rhdh-product-docs-1.8-Nov19-2025).
* **Generation Tool:** We used **[Ragas](https://docs.ragas.io/en/stable/concepts/test_data_generation/rag/)** (Testset Generation for RAG) to generate diverse Q&A pairs.
* **Evaluation Tool:** The evaluation was executed using the **[lightspeed-evaluation](https://github.com/lightspeed-core/lightspeed-evaluation)** tool, which consumes the dataset and calculates performance metrics.