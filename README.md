# RAcQUEt: Unveiling the Dangers of Overlooked Referential Ambiguity in Visual LLMs

This is the repository for the paper [RAcQUEt: Unveiling the Dangers of Overlooked Referential Ambiguity in Visual LLMs](https://aclanthology.org/2025.emnlp-main.1206/) (EMNLP 2025).

RAcQUEt is a carefully curated dataset designed to examine **referential ambiguity in image-based question answering** by introducing a testbed targeting distinct aspects of ambiguity. The dataset comprises **740 manually curated pairs** of images and ambiguous referential questions in English. RAcQUEt is publicly available at: [https://zenodo.org/records/17658707](https://zenodo.org/records/17658707).

---

## Dataset Structure and Contents

The RAcQUEt dataset is split into two main subsets, each provided as a separate JSONL file:

### 1. `racquet_general.jsonl`

This subset is designed to investigate referential ambiguity in **real-world images** sourced from **MSCOCO**.

* **Content:** 500 unique image-ambiguous question pairs.
* **Focus:** Referential ambiguity where an entity is unclear due to multiple potential candidates present in the image.

### 2. `racquet_bias.jsonl`

This subset is designed to analyze a critical, underexplored problem: how failing to address ambiguity leads to **stereotypical, socially biased responses**.

* **Content:** 240 unique image-ambiguous question pairs.
* **Focus:** Uses ad-hoc, generated images (with Dall-E 3) and questions that may trigger responses based on social biases and stereotypes if ambiguity is not recognized.

### Data Format

Both JSONL files follow the same structure, where each line is a JSON object containing the following keys:

* **`id`**: Unique ID for the image-question pair.
* **`image_url`**: URL pointing to the image (MSCOCO for GENERAL, Dall-E 3 generated for BIAS).
* **`question`**: The referentially ambiguous question.
* **`question_idx`**: A unique index for the question within a specific image.

 ---

## 📄 Paper Reference
```bibtex
@inproceedings{testoni-etal-2025-racquet,
    title = "{RA}c{QUE}t: Unveiling the Dangers of Overlooked Referential Ambiguity in Visual {LLM}s",
    author = "Testoni, Alberto and
    Plank, Barbara and
    Fern{\'a}ndez, Raquel",
    booktitle = "Proceedings of the 2025 Conference on Empirical Methods in Natural Language Processing",
    month = nov,
    year = "2025",
    address = "Suzhou, China",
    publisher = "Association for Computational Linguistics",
    url = "[https://aclanthology.org/2025.emnlp-main.1206/](https://aclanthology.org/2025.emnlp-main.1206/)",
    doi = "10.18653/v1/2025.emnlp-main.1206",
    pages = "23638--23658"
}
