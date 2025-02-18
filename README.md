# Reproducibility of "Evaluation of Reliability Criteria for News Publishers with Large Language Models"

## Overview

This repository contains the necessary resources and scripts to reproduce the results of the paper:

> **Evaluation of Reliability Criteria for News Publishers with Large Language Models**  
> **Authors**: Manuel Pratelli, John Bianchi, Fabio Pinelli, Marinella Petrocchi  
> DOI: [10.1145/3717867.3717924](https://doi.org/10.1145/3717867.3717924)

In this study, we investigate the use of a large language model (LLM) to assist in evaluating the reliability of online news publishers. Given the impracticality of relying solely on human experts for large-scale assessments, we evaluate the LLM’s ability to classify news articles according to expert-designed reliability criteria and compare its responses to those of human annotators.

Our dataset consists of **352 news articles**, annotated by **two human experts** and an **LLM-based annotator**. 
We assess agreement across **six reliability criteria**. In total we examine **6,081 annotations** on six criteria; additionally, a more detailed version of one of these criteria is considered, contributing 1,011 additional annotations.

### Key Findings:

- The LLM demonstrates **good agreement** with human annotators in three of the six criteria, including its ability to detect **negative targeting** in news content.
- For two additional criteria—**sensational language detection** and **bias recognition**—the LLM provides reasonable annotations, though with some trade-offs.
- The LLM helps resolve **disagreements** between human annotators, particularly in identifying **negative targeting cases**.

## Repository Contents

This repository provides the following resources:

- **`data/human_annotations.csv`** – Annotations produced by human experts.
- **`data/llm_annotations.csv`** – Annotations generated by the LLM-based annotator.
- **`data/articles_sample.csv`** – A sample of the news articles used in the study.
- **`experiments.ipynb`** – Script to compute inter-annotator agreement, confusion matrix by criteria and export human annotations in dis-agreement (to compare with expost-groundtruth and LLM-based annotator responses).
- **`prompts_generation.ipynb`** – The exact prompt used for collecting LLM-based annotations.
- **`outputs/human_experts_disagreements_{annotated, to_annotate}.csv`** – The manual annotation done in case of relevant dis-agreement.


## Citation

If you use this repository for your research, please cite:

@inproceedings{pratelli2025evaluation,
  author = {Pratelli, Manuel and Bianchi, John and Pinelli, Fabio and Petrocchi, Marinella},
  year = {2025},
  title = {Evaluation of Reliability Criteria for News Publishers with Large Language Models},
  publisher = {Association for Computing Machinery},
  booktitle = {Proceedings of the 17th ACM Web Science Conference 2025},
  url = {https://doi.org/10.1145/3717867.3717924},
  doi = {10.1145/3717867.3717924},
  series = {WEBSCI '25}
}
