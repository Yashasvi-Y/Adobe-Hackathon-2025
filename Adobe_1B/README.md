# Challenge 1B: Multi-Collection PDF Analysis

## 🧠 Overview  
This project presents an advanced PDF analysis pipeline capable of processing multiple document collections and extracting persona-based relevant sections based on predefined tasks or use cases. Each collection is driven by a specific persona and challenge ID, enabling accurate and contextual insights through structured JSON outputs.

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

| Collection         | Challenge ID   | Persona           | Task Description                                                                   | No. of PDFs |
|--------------------|----------------|-------------------|-------------------------------------------------------------------------------------|-------------|
| Travel Planning     | round_1b_002   | Travel Planner     | Plan a 4-day trip for 10 college friends to the South of France                    | 7           |
| Acrobat Learning    | round_1b_003   | HR Professional    | Create and manage fillable forms for employee onboarding and compliance            | 15          |

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

## ✨ Key Features

| Feature                       | Description                                                              |
| ----------------------------- | ------------------------------------------------------------------------ |
| 🎯 Persona-based Extraction   | Tailors information to the intent and profession of the user persona     |
| 📊 Section Importance Ranking | Ranks sections in order of relevance to the task                         |
| 📂 Multi-Collection Support   | Handles different domains/personas via modular collection folders        |
| 🧩 Modular and Extensible     | Easily add new challenges, personas, or domains                          |
| 📄 Structured JSON Output     | Output-ready format for downstream AI workflows and automation pipelines |
| 🔄 Offline and Configurable   | No external APIs; all logic handled locally for privacy and speed        |

---

## 🧪 Technologies Used

| Component          | Technology                          |
| ------------------ | ----------------------------------- |
| Language           | Python                              |
| PDF Parsing        | PyMuPDF / pdfminer.six / fitz       |
| JSON Configuration | Built-in `json` library             |
| Ranking Algorithm  | Custom heuristic / semantic scoring |
| Environment        | Offline / Local execution only      |

---

## 🚫 System Constraints

| Constraint                      | Details                                                                  |
| ------------------------------- | ------------------------------------------------------------------------ |
| 🔌 Offline Only                 | No external API calls or cloud dependencies                              |
| 📎 File Format Requirement      | Only `.pdf` files supported                                              |
| 📦 Folder Structure Enforcement | Must maintain folder and naming convention for each challenge/collection |
| 🧠 Semantic Inference Scope     | Limited to structural + keyword extraction; no generative AI inference   |

---

## 🧠 Tip for Success

Focus on:

* 🔍 Precision in extraction
* 🤖 Understanding the persona’s intent
* 📊 Structuring your results meaningfully

---

## 🏁 Submission

Each collection must include:

✅ `/PDFs/` folder with the source documents
✅ `challenge1b_input.json` file
✅ `challenge1b_output.json` file containing your extracted analysis

---

**Let’s scale smart document reading, one persona at a time!** 🧠📄🚀

```

