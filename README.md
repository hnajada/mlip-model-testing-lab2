Overview

In this lab you’ll evaluate a model with Zeno and use an LLM to generate targeted test cases.

Zeno: an interactive AI evaluation platform for exploring, debugging, and sharing model behavior across tasks and data types (e.g., chat, vision, audio).

LLM-generated tests: use an LLM to synthesize additional evaluation examples and stress specific model behaviors.



Learning goals

By the end, you will:

Spin up a local Zeno server and load a dataset, metrics, and model predictions.

Create and analyze slices (focused subsets of data) to uncover failure modes.

Use an LLM to generate new test cases for a chosen slice and reassess performance.




Deliverables

Zeno server running locally with the provided dataset, metrics, and model predictions visible.

Five (5) slices created in Zeno with meaningful insights you can articulate.

Three (3) proposed additional slices written down (what & why).

LLM test generation: pick one of your proposed slices and generate 10 new examples aligned with that slice, then re-evaluate and briefly summarize what changed.

Hint: For each slice, be ready to justify why you created it (hypothesis) and what you observed (evidence).



Getting started

Clone the starter repository.
The repo includes a Jupyter notebook with starter code.

Open the notebook and follow the scaffolded steps.



Environment & installation

Python: Use 3.10 (required for Zeno packages).

(Optional but recommended) Create a clean virtual environment:


python -m venv mlip-lab4
# Windows
mlip-lab4\Scripts\activate
# macOS/Linux
source mlip-lab4/bin/activate


Install dependencies:


pip install zenoml datasets transformers tqdm torch


Restart your notebook kernel after installing packages.



What to implement (in the notebook)

Complete all 7 steps outlined in the provided notebook. At a high level, you will:

Load the dataset.

Run (or import) model predictions.

Define metrics.

Launch Zeno and register your dataset/predictions/metrics.

Create at least 5 slices (e.g., by label, keyword, length, sentiment range, ambiguity).

Analyze slice-level behavior and record insights.

Use an LLM to generate targeted test cases for one proposed slice (10 examples), add them, and compare results.



Troubleshooting & fallbacks

Dataset/model issues? Use the provided tweets.csv in the folder as a fallback.

Zeno server won’t start? Open zenohub.py, copy its code into your notebook, and follow the inline steps to start the local server.

LLM access problems? If the preconfigured GPTs aren’t available, use plain ChatGPT to generate test cases consistent with your slice specification.



Deliverables to check

Zeno UI running locally with your dataset, predictions, and metrics visible.

Your 5 created slices and a concise explanation for each:

Why this slice?

What metric deltas or qualitative behaviors did you observe?

Your 3 proposed slices (written in the notebook/markdown cell).

The 10 LLM-generated examples for one proposed slice and the before/after comparison (metrics and/or qualitative notes).