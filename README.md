# client-risk-assessment-rag
AI-powered Retrieval-Augmented Generation (RAG) assistant that automates risk-assessment responses for IBM SaaS services using IBM Watson embeddings, Milvus vector database, and AWS Bedrock LLMs.
## ⚠️ Important Notice

This repository serves as a **technical portfolio demonstration** of a Retrieval-Augmented Generation (RAG) system I developed for client risk assessment. Due to confidentiality agreements:

- **No proprietary code** from the actual implementation is included
- **No client data** or sensitive information is present
- **Mock implementations** demonstrate architectural patterns and technical decisions
- **Real metrics and outcomes** are generalized or anonymized where included

The code examples here represent the **types of solutions** and **technical approaches** used in the production system, rewritten with synthetic data and generic use cases.

# 🧠 Client Risk Assessment RAG Assistant

## Overview
This project demonstrates a **Retrieval-Augmented Generation (RAG)** application built to automate and accelerate **security and compliance risk assessments** for IBM Apptio SaaS environments.  

The assistant uses **IBM embedding models**, a **Milvus vector database**, **IBM WatsonX Orchestrate** and **LLM running on AWS Bedrock LLMs** to retrieve relevant IBM SaaS ISO 27001 and SOC 2 control justifications and generate precise, context-aware responses to client questionnaires.  

This solution helps internal InfoSec teams respond faster to 4000+ customer security inquiries while maintaining high-quality, audit-ready answers.

---

## 🎯 Objectives
- Automate repetitive security questionnaire responses.  
- Enable **semantic retrieval** of justifications from SoA and SOC 2 datasets.  
- Replace traditional knowledge-base tools (e.g., Loopio), achieving > **$20K annual savings**.  
- Improve accuracy and turnaround time for client risk assessments.  

---

## 🏗️ Architecture

```mermaid
graph TD
    A[Customer Security Question] --> B[Watson Embedding Model]
    B --> C[Milvus Vector Database]
    C --> D[Retrieve Closest Matching Control Justifications]
    D --> E[LLM on AWS Bedrock]
    E --> F[Generated Context-Aware Response]
    F --> G[Watsonx Orchestrate UI / Slack Assistant]
