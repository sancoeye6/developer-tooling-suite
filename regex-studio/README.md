# Regex Studio v3.6 — Intelligent Data Parsing Engine

Regex Studio is a specialized offline ETL tool designed to clean, normalize, and structure unstructured HTML, MHTML, and text data for ingestion into analysis systems and Retrieval-Augmented Generation (RAG) pipelines.

It transforms messy exported content such as AI chats, LinkedIn feeds, and saved webpages into structured, machine-readable datasets.

---

## Purpose

Modern data sources often contain UI clutter, formatting noise, or embedded markup that makes them unsuitable for analysis or AI ingestion.

Regex Studio solves this by:

- Detecting source type automatically
- Extracting semantic content only
- Normalizing structure
- Preparing clean datasets for downstream systems

---

## Core Capabilities

### Smart Source Detection
Identifies content origin using pattern fingerprinting:
- LinkedIn HTML exports
- AI chat logs
- MHTML archives
- Raw HTML dumps

---

### Intelligent Parsing Engine
Instead of basic text stripping, Regex Studio:

- Builds a virtual DOM
- Queries semantic elements
- Falls back to regex extraction if needed
- Removes UI artifacts automatically

---

### AI Conversation Normalization
Standardizes different providers into a single format:

USER: text...

ASSISTANT: text...

Supports parsing formats from:
- ChatGPT
- Claude
- Gemini
- Generic HTML chat exports

---

### Code Block Preservation
All detected code blocks are wrapped safely:

[CODE] your code [/CODE]

This ensures code survives ingestion into downstream tools.

---

### Safety Panel (Token Monitoring)
Estimates token size and displays safety indicators for major LLM context windows.

Approximation:

tokens ≈ characters / 4

Threshold indicators:
- GPT safe zone
- Claude safe zone
- Gemini safe zone

---

### RAG Export Mode
Exports structured documents formatted for AI ingestion:

<source_document> <meta>

<title>filename</title>
<type>SOURCE_TYPE</type>
<date>YYYY-MM-DD</date>
</meta>
<content>
clean text
</content>
</source_document>
```This guarantees multi-document uploads remain logically separated when processed.


---

Workflow

1. Save webpage or chat as HTML or MHTML


2. Drag file into Regex Studio


3. System parses + cleans content


4. Review or edit text


5. Export structured dataset




---

Architecture

Design Philosophy: Freeze Logic Architecture

Meaning:

fully client-side

no backend

no uploads

runs offline

zero dependencies (optional PDF library only)



---

Tech Stack

Vanilla JavaScript

HTML5

CSS3

DOMParser API

FileReader API

Regex Engine

jsPDF (optional export)



---

Performance Characteristics

Instant parsing

Handles very large documents

Memory-efficient

No installation required

Runs in restricted environments



---

Use Cases

Preparing datasets for RAG pipelines

Cleaning exported chat logs

Structuring scraped content

Removing markup noise

Dataset preprocessing for analysis



---

Security

All processing occurs locally in the browser.

No data is:

uploaded

transmitted

stored externally

tracked



---

License

MIT License


---

Summary

Regex Studio is not a regex tester.

It is a structured data extraction engine disguised as a lightweight web app.

