# Machine Translation Pipeline Project

This repository contains a modular machine translation pipeline designed to translate text
from French to English using a HuggingFace model and to evaluate translation quality using
standard NLP metrics such as BLEU. The project is structured to be clear, extensible, and
aligned with good software engineering practices.

---

## 📌 Project Overview

The goal of this project is to implement a complete translation workflow, including:

- loading input data,
- applying a machine translation model,
- processing translated outputs,
- evaluating translation quality,
- saving results to an output directory.

The pipeline is orchestrated by a central `Orchestrator` class that coordinates all steps.

---

## 📁 Project Structure

project/
│
├── data/                # Input data (CSV, JSON, etc.)
│   ├── sample.json
│   ├── sample02.json
│   └── big.csv
│
├── output/              # Generated outputs
│
├── src/
│   ├── loaders/         # Data loading modules
│   ├── translators/     # HuggingFace translation models
│   ├── processors/      # Optional text processing steps
│   ├── evaluators/      # Evaluation metrics (BLEU, etc.)
│   └── orchestrator/    # Main pipeline controller
│       └── orchestrator.py
│
└── main.py (optional)   # Entry point for running the pipeline


---

## ⚙️ How the Pipeline Works

The `Orchestrator` class performs the following steps:

1. **Load data** from the specified file (CSV or JSON).
2. **Translate text** using the model  
   `Helsinki-NLP/opus-mt-fr-en`.
3. **Process results** (optional transformations).
4. **Evaluate translations** using BLEU or another metric.
5. **Save outputs** to the `output/` directory.
6. **Print evaluation scores** and completion status.

Example execution:

```python
if __name__ == "__main__":
    orch = Orchestrator(
        data_path="big.csv",
        output_dir="output",
        translation_model="Helsinki-NLP/opus-mt-fr-en",
        metric="bleu"
    )
    orch.run()
```
## 🎯 Learning Objectives
By working with this project, students will practice:

- structuring a Python project using modular architecture,
- working with HuggingFace translation models,
- handling text datasets,
- computing translation quality metrics,
- managing a complete NLP pipeline from input to evaluation.

## 🧩 Assignment Instructions
You must use this repository as the source code for your assignment:

👉 https://github.com/delnouty/bidabi-project-03.git (github.com in Bing)

Your task is to:

- Generate a new project using the provided template.
- Clone this repository.
- Transfer the code from this repository into the structure created by your template.
- Adapt the code where necessary to match the template’s conventions.
- Ensure the pipeline runs correctly inside the new project.

You are expected to demonstrate initiative and independent problem‑solving while integrating the code.

📅 Your results will be reviewed during the next session.

## 🚀 Running the Project
After integrating the code into your template:
```Bash
python -m venv .venv
source .venv/bin/activate   # or .venv\Scripts\Activate.ps1 on Windows
pip install -r requirements.txt
python src/orchestrator/orchestrator.py
```
## 📄 License
This project is provided for educational purposes.  
