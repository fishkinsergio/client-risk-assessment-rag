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
🎯 The Problem
Risk assessment teams struggled with:

Manual document analysis across 20+ sources per assessment
2-3 days per assessment (100 questions) of continuous work
Aggressive deadlines from regulators, auditors, and clients
Scalability limits during peak assessment periods

Traditional search tools and knowledge bases couldn't synthesize information or provide direct answers—analysts still had to read and interpret multiple documents.
Read detailed business problem analysis →

📊 Project Impact

95%+ reduction in query response time (days → minutes)
Processed 1,000+ risk assessment documents
95%+ accuracy on internal evaluation benchmark
Deployed to 10+ risk internal IBM analysts
3-4x capacity increase with same team size

## 🎯 Objectives
- Automate repetitive security questionnaire responses.  
- Enable **semantic retrieval** of justifications from SoA and SOC 2 datasets.  
- Replace traditional knowledge-base tools (e.g., Loopio), achieving > **$20K annual savings**.  
- Improve accuracy and turnaround time for client risk assessments.  

---
Documents → Document Processing → Embedding Generation → Vector Database (Milvus)
                                                                ↓
User Query → Query Processing → Semantic Search → Context Retrieval
                                                                ↓
                                            Prompt Construction → LLM Generation
                                                                ↓
                                        Answer + Citations → Quality Validation → User

Key Components:

Document Ingestion: Multi-format processing with Docing (IBM RedHat)
Vector Database: Milvus via IBM Watson.data
LLM Orchestration: IBM WatsonX Orchestrate
Infrastructure: AWS (IBM-managed VPC) with CloudWatch monitoring

View detailed architecture documentation →

👨‍💻 My Technical Contributions
I owned end-to-end implementation from data preparation through production deployment:
1. Data Ingestion Pipeline

Architected document processing using Docing for multi-format conversion (PDF, DOCX, XLSX, HTML)
Developed layout-aware extraction preserving tables and complex structures
Processed 10,000+ documents with 98%+ extraction accuracy

2. Vector Database Architecture

Provisioned and configured Milvus vector database via IBM Watson.data
Designed "universe schema" supporting dynamic ingestion without schema migrations
Optimized indexing strategy for <100ms retrieval latency at scale

3. RAG Pipeline & Prompt Engineering

Integrated Milvus with IBM WatsonX Orchestrate
Designed hybrid retrieval strategy (semantic + keyword + metadata filtering)
Developed prompt engineering framework achieving 95%+ answer quality

4. Production Deployment & Monitoring

Deployed within IBM-managed AWS VPC infrastructure
Configured AWS CloudWatch for comprehensive observability
Maintained 99.5%+ uptime with <200ms p95 end-to-end latency

Read detailed technical contributions →
