# Context-Aware Course Transcript Q&A System

## Overview

Built a Retrieval-Augmented Generation (RAG) system to answer questions from online course transcripts using retrieved transcript context.

## Problem

General-purpose LLMs may not have access to specific information available in course transcripts. This project retrieves relevant transcript content and provides it to the LLM as context to generate course-specific answers.

## Workflow

```text
Course Transcripts
       ↓
Document Loading
       ↓
Text Splitting / Chunking
       ↓
Embeddings
       ↓
Chroma Vector Database
       ↓
Semantic Retrieval
       ↓
Relevant Context
       ↓
OpenAI LLM
       ↓
Course-Specific Answer
```

## Technologies

* Python
* LangChain
* OpenAI
* Chroma
* Embeddings
* Retrieval-Augmented Generation (RAG)
* Large Language Models (LLMs)
* Semantic Search
* Prompt Engineering

## Result

Enabled course-specific answers using transcript data beyond the LLM's pretrained knowledge.

## Project Structure

```text
notebooks/
└── course_transcript_rag.ipynb

README.md
requirements.txt
.gitignore
```

## Setup

```bash
pip install -r requirements.txt
```

Create a `.env` file and add your OpenAI API key:

```text
OPENAI_API_KEY=your_api_key
```

Do not commit the `.env` file to GitHub.

## Example

**User Query:**

```text
What is retrieval augmented generation?
```

The system retrieves relevant transcript chunks from the vector database and passes them as context to the LLM to generate the answer.
