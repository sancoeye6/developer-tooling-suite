# Regex Studio | Structured Data Extraction Engine

**Offline ETL Processor for Cleaning and Structuring Unstructured Web Data**  
Single-File • Zero Backend • RAG-Optimized • Privacy-First

![Type](https://img.shields.io/badge/type-offline--etl-blue)
![Architecture](https://img.shields.io/badge/architecture-client--side-green)
![Dependencies](https://img.shields.io/badge/dependencies-none-orange)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## 🎯 What It Does

Regex Studio is a specialized offline ETL engine that transforms messy exported content into clean, structured, machine-readable datasets ready for analysis or AI ingestion.

It processes sources like:
- AI chat exports  
- LinkedIn pages  
- Saved websites  
- Raw HTML dumps  
- MHTML archives  

The system extracts **semantic content only** and removes UI clutter, formatting noise, and markup artifacts.

---

## 🧩 The Problem It Solves

Modern exported data is rarely analysis-ready. It often contains:

- UI buttons
- navigation elements
- styling markup
- embedded scripts
- tracking tags
- formatting junk

These make datasets unusable for:

- analytics
- automation
- LLM ingestion
- RAG pipelines

Regex Studio converts noisy exports into structured datasets instantly.

---

## ⚙ Core Capabilities

### Smart Source Detection
Automatically fingerprints files to determine origin type:

- LinkedIn exports
- AI chat logs
- HTML pages
- MHTML archives
- generic raw dumps

---

### Intelligent Parsing Engine
Instead of basic text stripping, the engine:

- builds a virtual DOM
- queries semantic nodes
- extracts meaningful text
- removes UI artifacts
- falls back to regex extraction when DOM parsing fails

---

### AI Conversation Normalization
Converts multiple AI formats into a unified schema:

USER: message ASSISTANT: response

Supports parsing formats from:

- ChatGPT
- Claude
- Gemini
- generic chat HTML exports

---

### Code Block Preservation
All detected code blocks are wrapped safely:

[CODE] your code [/CODE]

This guarantees code survives ingestion into downstream systems.

---

### Safety Panel (Token Monitoring)

Provides real-time token estimation:

tokens ≈ characters ÷ 4

Displays safety indicators for:

- GPT context windows
- Claude limits
- Gemini limits

Helps prevent dataset overflow during AI ingestion.

---

### RAG Export Mode

Exports structured documents optimized for AI ingestion:

<source_document>

<title>filename</title>
<type>SOURCE_TYPE</type>
<date>YYYY-MM-DD</date>
<content>clean text</content>
</source_document>
```This ensures multi-document uploads remain logically separated inside vector or RAG systems.


---

🔄 Workflow

1. Save webpage or chat as HTML or MHTML


2. Drag file into Regex Studio


3. Engine detects format automatically


4. Content is parsed and cleaned


5. User reviews or edits text


6. Export structured dataset




---

🧠 Architecture

Design Philosophy: Freeze-Logic Architecture

Meaning:

fully client-side processing

no backend

no uploads

runs offline

portable single file



---

🛠 Tech Stack

HTML5

CSS3

Vanilla JavaScript

DOMParser API

FileReader API

Regex Engine

jsPDF (optional export module)



---

⚡ Performance Characteristics

instant parsing

handles large documents

memory efficient

zero install

works in restricted environments

runs on low-spec machines



---

🧪 Use Cases

preparing datasets for RAG pipelines

cleaning exported chat logs

structuring scraped content

preprocessing datasets for analysis

removing markup noise

archiving conversations



---

🔒 Security

All processing happens locally in the browser.

No data is:

uploaded

transmitted

stored externally

tracked



---

📄 License

MIT License — free to use, modify, and distribute.


---

🧾 Summary

Regex Studio is not a regex tester.

It is a structured data extraction engine disguised as a lightweight web application.
