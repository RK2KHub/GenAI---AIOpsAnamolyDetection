# MLOpsAnamolyDetection
---
# AIOps Log Parsing
## Objective

The objective of this study is to assess the capability of ChatGPT, a state-of-the-art large language model, in the domain of automated log parsing for software engineering tasks. Software logs are crucial for ensuring the reliability and maintainability of large-scale software systems by providing essential runtime information. Log parsing involves converting unstructured log messages into structured data, which is vital for tasks such as anomaly detection, failure prediction, and security monitoring.

## Research Questions

This study addresses two key research questions:

1. Can ChatGPT effectively perform log parsing?
2. How does ChatGPT perform with different prompting methods?

## Methodology

In this study, we replicated a preliminary evaluation of ChatGPT for log parsing. We compare the performance of ChatGPT with two other state-of-the-art log parsing tools: AEL and Drain. The evaluation uses six representative log datasets from various systems, each containing 2,000 manually labeled log messages.

## Setup Instructions

### ChatGPT

1. Navigate to `log-analytics-chatgpt-master`.
2. Set the OpenAI API Key at `/chat/__init__.py` (`OPEN_AI_KEY`).
3. Run the script:
   ```bash
   python main.py
   ```
   to generate log templates with ChatGPT.
4. Set the output directory at `/outputs/post_process.py` and run:
   ```bash
   cd outputs && python post_process.py
   ```
   to apply common post-process rules for log parsing.
5. Set the output directory in `evaluate.py` and run:
   ```bash
   python evaluate.py
   ```
   to evaluate ChatGPT's performance.

### AEL

1. Navigate to `logparser-main/logparser-main/logparser/AEL`.
2. Run the benchmark script:
   ```bash
   python benchmark.py
   ```

### Drain

1. Navigate to `logparser-main/logparser-main/logparser/Drain`.
2. Run the benchmark script:
   ```bash
   python benchmark.py
   ```

## Datasets

The evaluation uses the following datasets:

- OpenStack (distributed systems)
- BGL (supercomputers)
- Linux (operating systems)
- Android (mobile systems)
- Apache (server applications)
- Proxifier (standalone software)

Each dataset contains 2,000 manually labeled log messages and originated from LogPAI.

---

This `Readme.md` file provides an overview of the repository, its objectives, methodology, setup instructions for running benchmarks, and details about the datasets used in the evaluation. Adjust paths and commands as necessary for your specific setup.
