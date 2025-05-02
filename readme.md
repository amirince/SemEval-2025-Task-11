# 🧠 Combining Expert Personas via Prompting for Enhanced Multilingual Emotion Analysis

This repository contains our submission for [SemEval 2025 Task 11](https://github.com/emotion-analysis-project/SemEval2025-Task11) by Team **AI4PC**. Our system employs a multi-expert architecture consisting of four specialized "juror" models that independently analyze a text sample for emotion and reasoning. These outputs are then aggregated by a "judge" model that makes the final emotion classification.

---

## 🚀 Getting Started

### ✅ Prerequisites

To run the project, you'll need:

- [**Ollama**](https://ollama.com/): Install the Ollama application for your platform and pull the necessary models for both the judge and jurors.
- A machine with sufficient compute to run the selected LLMs.
- Python 3.12.1 (recommended)

### 📁 Project Structure

| File / Folder               | Description |
|----------------------------|-------------|
| `config.py`                | Defines key configurations such as model names, datasets, and target emotions. |
| `templates.py`             | Contains prompt templates for the judge and jurors, into which data and examples are injected. |
| `example_analysis_pipeline.py` | Backend logic to interact with the Ollama models and coordinate communication between jurors and judge. |
| `main.py`                  | The main pipeline to run the full analysis. It first runs the jurors, saves intermediate outputs, then invokes the judge. |
| `data/`                    | Contains datasets provided by SemEval organizers. |
| `lang_detect/`             | Custom language detection module tailored for this task. |

---

### 🛠️ How to Run

1. **Clone** the repository:
   ```bash
   git clone https://github.com/amirince/SemEval-2025-Task-11.git
2. **Create a virtual environment** and activate it:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
4. **Configure parameters** in config.py to match your desired setup.
5. **Run** the main pipeline:
    ```bash
    python main.py
    ```
    - ⏳ This process may take a while depending on your compute capacity.

## 👥Author:
- Amir Ince