# 🧠 Challenge 1b: Multi-Collection PDF Analysis

## 🚀 Overview

This project presents a powerful **PDF analysis solution** capable of handling multiple document collections. It extracts relevant and ranked information tailored to user **personas** and **job-to-be-done** use cases. The output is a structured JSON providing both metadata and deep content insights from the PDFs.

---

## 🧾 Project Structure

```

Challenge\_1b/
├── Collection 1/
│   ├── PDFs/                     # Travel Planning PDFs
│   ├── challenge1b\_input.json   # Input config for Collection 1
│   └── challenge1b\_output.json  # Output results
├── Collection 2/
│   ├── PDFs/                     # Adobe Acrobat Learning PDFs
│   ├── challenge1b\_input.json   # Input config for Collection 2
│   └── challenge1b\_output.json  # Output results
├── Collection 3/
│   ├── PDFs/                     # Recipe Collection PDFs
│   ├── challenge1b\_input.json   # Input config for Collection 3
│   └── challenge1b\_output.json  # Output results
└── README.md

````

---

## 📚 Collections Breakdown

| Collection | Challenge ID    | Persona           | Task Description                                                                 | Documents         |
|------------|------------------|-------------------|----------------------------------------------------------------------------------|--------------------|
| Collection 1 | `round_1b_002` | Travel Planner     | Plan a 4-day trip to the South of France for 10 college friends                 | 7 travel guides    |
| Collection 2 | `round_1b_003` | HR Professional    | Create and manage fillable forms for onboarding and compliance                  | 15 Acrobat guides  |
| Collection 3 | `round_1b_001` | Food Contractor    | Design a vegetarian buffet-style dinner menu for a corporate gathering          | 9 cooking guides   |

---

## 🧩 Input Format (`challenge1b_input.json`)

```json
{
  "challenge_info": {
    "challenge_id": "round_1b_XXX",
    "test_case_name": "specific_test_case"
  },
  "documents": [
    {
      "filename": "sample.pdf",
      "title": "Document Title"
    }
  ],
  "persona": {
    "role": "User Persona"
  },
  "job_to_be_done": {
    "task": "Use case description"
  }
}
````

---

## 📤 Output Format (`challenge1b_output.json`)

```json
{
  "metadata": {
    "input_documents": ["doc1.pdf", "doc2.pdf"],
    "persona": "Travel Planner",
    "job_to_be_done": "Plan 4-day trip"
  },
  "extracted_sections": [
    {
      "document": "doc1.pdf",
      "section_title": "Day 1 Itinerary",
      "importance_rank": 1,
      "page_number": 3
    }
  ],
  "subsection_analysis": [
    {
      "document": "doc1.pdf",
      "refined_text": "Suggested travel route and accommodation options",
      "page_number": 3
    }
  ]
}
```

---

## ✨ Key Features

* ✅ **Multi-collection PDF ingestion**
* 🧠 **Persona-based context filtering**
* 🔍 **Importance-based section ranking**
* 🧾 **Refined content summaries per section**
* 💾 **Clean and structured JSON output**

---

## 📌 Sample Use Case

> **Persona:** Travel Planner
> **Job To Be Done:** Plan a detailed trip itinerary
> **Expected Output:** Ranked list of day-wise trip activities, maps, transportation tips, and hotel recommendations extracted from relevant travel guides.

---

## 💻 Run Instructions

No code execution is required for this challenge – your role is to create the correct `input.json`, analyze the PDFs manually or programmatically, and fill the `output.json` in the given format.

---

## 📎 Notes

* Output must match the **structure exactly** as per challenge requirement.
* You may automate analysis or fill outputs manually using PDF readers.
* Always rank sections by **relevance to persona's task**, not by appearance.

---

## 🧠 Tip for Success

Focus on:

* 🔎 Precision in extraction
* 🤖 Understanding the persona’s intent
* 📊 Structuring your results meaningfully

---

## 🏁 Submission

Each collection must include:

* ✅ `/PDFs/` folder with source documents
* ✅ `challenge1b_input.json` file
* ✅ `challenge1b_output.json` with your extracted analysis

---

