# RAG-powered Material Insight Tool

This is a research project that combines semantic search and natural language generation to answer queries about material strength based on a structured dataset.

## 🧠 Overview

The tool enables users to ask natural language questions such as:

- *What is the strength of Steel SAE 1040 normalized?*
- *What is the yield strength of Steel SAE 1050 annealed?*

The system performs the following steps:
1. Encodes the query using a SentenceTransformer to find the most semantically relevant context.
2. Passes this context along with the query to a language model to generate an answer.
3. Returns the actual strength value from the data for transparency.

---

## ⚙️ Technical Details

- **Semantic Search:** `all-MiniLM-L6-v2` from SentenceTransformers
- **Generator Model:** `google/flan-t5-base` via HuggingFace Transformers
- **Frontend:** Built with Gradio for a simple and interactive UI
- **Dataset:** Contains material properties including:
  - Material name
  - Heat treatment
  - Strength (Su)
  - Yield strength (Sy)
  - Elongation (A5)
  - Hardness (Bhn)

---

## 📁 Project Structure

- `app.py` — Main application logic (UI, retrieval, generation)
- `Data.csv` — Dataset used to retrieve strength data
- `requirements.txt` — All dependencies to recreate the environment
- `screenshot.png` — Preview of the tool's interface

---

## 🚀 Running Locally

1. Clone the repository:
```bash
git clone https://github.com/yourusername/material-insight-tool.git
cd material-insight-tool
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Make sure `Data.csv` is in the same directory.

4. Run the app:
```bash
python app.py
```

5. Open your browser at `http://127.0.0.1:7860` to use the app.

---

## 🔍 Sample Queries

| Query                                                  | Strength (MPa) |
|--------------------------------------------------------|----------------|
| What is the strength of Steel SAE 1040 normalized?     | 647.11         |
| What is the yield strength of Steel SAE 1050 annealed? | 537.16         |

---

## 🖼️ User Interface

![App Screenshot](screenshot.png)

---

## 👤 Author

**Hassan Mahmood Yousafzai**  
📧 hassan.yousafzai@gmail.com  
🔗 [linkedin.com/in/hassan-yousafzai](https://linkedin.com/in/hassan-yousafzai)

---

## 📄 License

This project is licensed under the MIT License.
