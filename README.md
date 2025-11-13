#  Multi-Agent Debate System (Mistral Edition)

A modern NLP project demonstrating **multi-agent interaction** with Large Language Models (LLMs).  
Three agents — **PRO**, **CON**, and **MODERATOR** — debate on a given topic and collaboratively produce a reasoned conclusion.  

Built with the open-source model **Mistral-7B-Instruct-v0.2**, it showcases autonomous reasoning, role-based prompting, and conversational orchestration in Python.

---

## Overview

This project simulates a **self-contained debate** between AI agents.  
Each agent has a distinct role:
- 🟢 **PRO** — argues *for* the topic  
- 🔴 **CON** — argues *against* the topic  
- ⚖️ **MODERATOR** — summarizes and decides who presented stronger arguments  

It’s a minimal, readable, and fully open implementation of multi-agent collaboration using Hugging Face and `transformers`.

---

##  Features

- Three autonomous agents interacting through prompts  
- Reasoning and counter-argument generation  
- Text-based output of debate rounds  
- Works locally or in Google Colab  
- Uses **Mistral-7B-Instruct-v0.2**, an open and high-quality instruction model  

---

## Example Output
Topic: Should AI replace teachers?
🟢 PRO:
AI can provide personalized learning experiences and adapt to each student's pace.
🔴 CON:
AI lacks human empathy and cannot fully replace the emotional connection of real teachers.
⚖️ MODERATOR:
Both sides raise strong points. While AI enhances accessibility, it cannot replace human mentorship.
Winner: Draw.


---

## Tech Stack

| Component | Description |
|------------|--------------|
| **Language** | Python 3.12+ |
| **Model** | `mistralai/Mistral-7B-Instruct-v0.2` |
| **Frameworks** | Hugging Face `transformers`, `accelerate` |
| **Interface (optional)** | Streamlit or Google Colab |
| **Platform** | Local / Colab Free GPU |

---

## � How It Works

1. Each agent is assigned a role and prompt template.  
2. The `PRO` and `CON` agents independently generate their arguments.  
3. The `MODERATOR` reviews both and writes a neutral conclusion.  
4. The system loops through several rounds to simulate discussion.

This design mimics reasoning chains and shows how LLMs can self-reflect and cooperate.

---

## How to Run

### Option 1 — Run in Google Colab
1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new notebook and copy the code from `multi_agent_debate.ipynb`.
3. Add your [Hugging Face token](https://huggingface.co/settings/tokens).
4. In Colab, set:
   _Runtime → Change runtime type → GPU → Save_
5. Run all cells and enter a topic for the debate.

### Option 2 — Run Locally
```bash
pip install transformers huggingface_hub accelerate
python multi_agent_debate.py

