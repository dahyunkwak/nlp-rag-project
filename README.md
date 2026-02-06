# nlp-rag-project
Domain-specific RAG pipeline for question answering with retrieval strategy experiments
## Project Overview
본 프로젝트는 **학칙 문서 기반 질의응답(QA)** 을 목표로 한  
Retrieval-Augmented Generation (RAG) 시스템을 구현하고,
검색 전략 개선을 통해 응답의 정확성과 근거성을 향상시키는 것을 목표로 합니다.

- **Domain**: University policy documents (public samples), MMLU PRO
- **External Knowledge**: Wikipedia (via API)
- **Task**: Domain-specific Question Answering
- **Language**: Python

- ## Key Ideas
- Vector-based document retrieval with FAISS
- External knowledge augmentation using Wikipedia API
- Prompt design for grounded, citation-aware generation
- Comparison between baseline and improved retrieval strategies

## System Pipeline
1. **Document Preprocessing**
   - Publicly available university policy samples
   - Text cleaning & chunking
2. **Embedding & Vector Store**
   - Sentence embedding
   - FAISS-based vector indexing
3. **Query-time Retrieval**
   - Top-k similarity search
   - Retrieval strategy refinement
4. **Answer Generation**
   - LLM-based response generation with retrieved context
5. **Evaluation**
   - Qualitative comparison
   - Retrieval relevance & answer faithfulness analysis

##  Implementation Details
- **LLM**: Upstage Solar Pro 2
- **Embedding**: Upstage embeddings
- **Vector Store**: FAISS
- **External Knowledge**: Wikipedia API
- **Pipeline Style**: Custom RAG implementation (not end-to-end framework)

##  Experiments & Results
- 25/25 in EWHA 21/25 in MMLU PRO
- Improved retrieval shows:
  - More relevant context selection
  - Reduced hallucination in answers
  - Better alignment with policy documents
