# Challenge 1B: Multi-Collection PDF Analysis

🧠 **Overview**  
This project presents an advanced PDF analysis pipeline capable of processing multiple document collections and extracting persona-based relevant sections based on predefined tasks or use cases. Each collection is driven by a specific persona and challenge ID, enabling accurate and contextual insights through structured JSON outputs.

---

### ✨ Key Features | 🛠 Technologies Used | 🚫 System Constraints

| ✨ Key Features                                                                 | 🛠 Technologies Used                       | 🚫 System Constraints                                                                 |
|--------------------------------------------------------------------------------|-------------------------------------------|----------------------------------------------------------------------------------------|
| 📂 Multi-collection persona-based PDF analysis                                 | Python (PyMuPDF, pdfplumber, fitz)        | ❌ No cloud API or online model use allowed                                            |
| 🔍 Contextual section identification using task descriptions                   | Regex, spaCy, NLTK                        | ❌ Output must be generated fully offline                                              |
| 📊 Importance ranking of extracted content                                     | Custom ranking heuristics                 | ❌ Fixed folder structure for each collection (`PDFs/`, `input.json`, `output.json`)   |
| 🧠 Role-specific extraction logic via persona-task matching                     | JSON Schema, Rule-based filtering          | ❌ Uniform output JSON structure as per problem description                            |
| 🧩 Extensible architecture for scaling across more collections and personas     | Modular Python scripts                    | ❌ External library usage limited to lightweight, offline-compatible ones              |

---

## 📁 Project Structure

```

Challenge\_1b/
├── Collection 1/                   # Travel Planning
│   ├── PDFs/                      # South of France travel guides
│   ├── challenge1b\_input.json     # Input configuration for analysis
│   └── challenge1b\_output.json    # Extracted results
├── Collection 2/                   # Adobe Acrobat Learning
│   ├── PDFs/                      # Acrobat tutorials and manuals
│   ├── challenge1b\_input.json     # Input configuration for analysis
│   └── challenge1b\_output.json    # Extracted results
└── README.md

````

---

## 📚 Collections Overview

| Collection        | Challenge ID   | Persona           | Task Description                                                             | No. of PDFs |
|------------------|----------------|-------------------|------------------------------------------------------------------------------|-------------|
| Travel Planning   | round_1b_002   | Travel Planner    | Plan a 4-day trip for 10 college friends to the South of France              | 7           |
| Acrobat Learning  | round_1b_003   | HR Professional   | Create and manage fillable forms for employee onboarding and compliance      | 15          |

---

## 📥 Input JSON Format

```json
{
  "challenge_info": {
    "challenge_id": "round_1b_XXX",
    "test_case_name": "specific_test_case"
  },
  "documents": [
    {"filename": "doc1.pdf", "title": "PDF Title"}
  ],
  "persona": {
    "role": "User Persona"
  },
  "job_to_be_done": {
    "task": "Use case or task description"
  }
}
````

---

## 📤 Output JSON Format

```json
{
  "metadata": {
    "input_documents": ["doc1.pdf", "doc2.pdf"],
    "persona": "User Persona",
    "job_to_be_done": "Task description"
  },
  "extracted_sections": [
    {
      "document": "doc1.pdf",
      "section_title": "Relevant Section Title",
      "importance_rank": 1,
      "page_number": 3
    }
  ],
  "subsection_analysis": [
    {
      "document": "doc1.pdf",
      "refined_text": "Summarized or relevant content text here...",
      "page_number": 3
    }
  ]
}
```

---

## 📌 Notes

* Ensure each collection follows the expected input/output format before running the pipeline.
* Designed with modularity and clarity to support evaluation across multiple challenges in the hackathon.

---

## 🧠 Tip for Success

Focus on:

* 🔎 Precision in extraction
* 🤖 Understanding the persona’s intent
* 📊 Structuring your results meaningfully

---

## 🏁 Submission

Each collection must include:

✅ `/PDFs/` folder with the source documents
✅ `challenge1b_input.json` file
✅ `challenge1b_output.json` with your extracted analysis

---

**Let’s decode PDFs at scale — fast, structured, offline.** 🚀📄

```


