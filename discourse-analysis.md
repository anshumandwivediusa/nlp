# Discourse Analysis in Natural Language Processing (NLP)

## Overview

**Discourse Analysis** is the branch of Natural Language Processing (NLP) that studies how multiple sentences are connected to form a coherent conversation, paragraph, or document.

Unlike **Lexical Analysis**, **Syntactic Analysis**, or **Semantic Analysis**, which primarily focus on individual words or single sentences, Discourse Analysis examines relationships **across sentences**.

It enables NLP systems to understand:

- Who or what pronouns refer to.
- How ideas are connected.
- The flow of a conversation.
- Context maintained throughout a document.
- Logical relationships between sentences.

Discourse Analysis is fundamental to modern applications such as **chatbots, virtual assistants, document summarization, question answering, Retrieval-Augmented Generation (RAG), and Large Language Models (LLMs).**

---

# Objectives

- Understand relationships across multiple sentences.
- Resolve references to entities.
- Maintain conversational context.
- Identify logical discourse relationships.
- Improve coherence and document understanding.

---

# Where Discourse Analysis Fits in the NLP Pipeline

```text
Raw Text
    │
    ▼
Text Preprocessing
    │
    ▼
Lexical Analysis
    │
    ▼
Syntactic Analysis
    │
    ▼
Semantic Analysis
    │
    ▼
Discourse Analysis
    │
    ▼
Pragmatic Analysis
```

---

# Example Paragraph

```text
Satya Nadella announced a new AI platform.
He said it would improve developer productivity.
The announcement was made during Microsoft Build.
```

To understand this paragraph, an NLP system must determine:

- **He** refers to **Satya Nadella**.
- **it** refers to the **AI platform**.
- Sentence 2 elaborates on Sentence 1.
- Sentence 3 provides additional context.

---

# Core Techniques

## 1. Coreference Resolution

### Definition

Coreference Resolution identifies when multiple words or phrases refer to the **same real-world entity**.

It answers questions like:

- Who does **he** refer to?
- What does **it** refer to?

---

### Example

**Input**

```text
Satya Nadella announced a new AI platform.
He introduced it during Microsoft Build.
```

**Output**

```text
He  → Satya Nadella
it  → AI platform
```

---

### Applications

- Question Answering
- Chatbots
- Information Extraction
- Knowledge Graph Construction
- Document Summarization

---

## 2. Context Tracking

### Definition

Context Tracking maintains the current topic, entities, and conversation state across multiple sentences or dialogue turns.

Without context tracking, conversational systems would lose track of previous information.

---

### Example

```text
User:
Tell me about Microsoft.

Assistant:
Microsoft is a technology company.

User:
Who is its CEO?
```

**Output**

```text
its → Microsoft
CEO → Satya Nadella
```

The assistant remembers that **its** refers to **Microsoft**.

---

### Applications

- Conversational AI
- Chatbots
- Virtual Assistants
- Customer Support Systems
- Multi-turn Question Answering

---

## 3. Discourse Parsing

### Definition

Discourse Parsing identifies the **logical relationships between sentences or clauses**.

Instead of analyzing grammar, it explains how ideas connect.

Common discourse relations include:

- Cause
- Effect
- Contrast
- Elaboration
- Explanation
- Sequence
- Condition

---

### Example 1 (Cause)

```text
The roads were flooded.
Therefore, schools remained closed.
```

Relationship

```text
Cause
    │
    ▼
Effect
```

---

### Example 2 (Elaboration)

```text
Microsoft released a new AI model.
It performs better than the previous version.
```

Relationship

```text
Sentence 2
      │
Elaborates
      │
Sentence 1
```

---

### Applications

- Text Summarization
- Reading Comprehension
- Document Understanding
- Essay Analysis
- Legal Document Processing

---

# Comparison of Techniques

| Technique | Purpose | Example |
|------------|---------|---------|
| **Coreference Resolution** | Resolves references to the same entity | `He → Satya Nadella` |
| **Context Tracking** | Maintains context across multiple sentences or conversations | `its → Microsoft` |
| **Discourse Parsing** | Identifies logical relationships between sentences | Cause, Contrast, Elaboration |

---

# Real-World Example

## Input

```text
Microsoft announced Copilot.
The company said it would improve developer productivity.
Customers welcomed the announcement because it simplifies daily tasks.
```

### Coreference Resolution

```text
The company → Microsoft

it → Copilot
```

### Context Tracking

```text
Topic:
Microsoft → Copilot → Developer Productivity
```

### Discourse Parsing

```text
Sentence 2
      │
Elaboration
      │
Sentence 1

Sentence 3
      │
Cause
      │
Sentence 2
```

---

# Industry Applications

| Domain | Usage |
|---------|-------|
| Chatbots | Maintain conversation context |
| Virtual Assistants | Understand follow-up questions |
| Search Engines | Better document understanding |
| Question Answering | Resolve ambiguous references |
| Document Summarization | Produce coherent summaries |
| Machine Translation | Preserve context across sentences |
| Healthcare | Understand long clinical notes |
| Legal AI | Analyze contracts and legal documents |
| Retrieval-Augmented Generation (RAG) | Maintain context across retrieved documents |

---

# Traditional NLP vs Modern LLMs

| Technique | Traditional NLP | Modern LLMs |
|------------|-----------------|-------------|
| Coreference Resolution | ✅ Explicit models | ✅ Learned implicitly |
| Context Tracking | Limited | Extensive long-context reasoning |
| Discourse Parsing | Research-intensive | Often implicit within Transformer models |

Modern Large Language Models learn many discourse relationships automatically through self-attention, but explicit discourse analysis remains valuable for explainability, information extraction, long-document understanding, and enterprise NLP applications.

---

# Best Practices

- Perform Discourse Analysis **after Semantic Analysis**.
- Resolve entity references before extracting relationships.
- Maintain conversation state in dialogue systems.
- Preserve document context for long-form reasoning.
- Combine discourse analysis with retrieval for RAG systems.

---

# Summary

Discourse Analysis helps NLP systems move beyond understanding **individual sentences** to understanding **entire conversations and documents**.

Its three primary techniques are:

- **Coreference Resolution** – Determines which words refer to the same entity.
- **Context Tracking** – Maintains context across multiple sentences or dialogue turns.
- **Discourse Parsing** – Identifies logical relationships between sentences.

Together, these techniques enable NLP systems to produce coherent, context-aware, and logically consistent outputs, making them essential for modern AI applications such as chatbots, question answering, document summarization, and Retrieval-Augmented Generation (RAG).
