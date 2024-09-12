# HeReFaNMi RAG API 🚀

**HeReFaNMi (Health-Related Fake News Mitigation)** is an AI-powered system developed to identify and mitigate fake news in the healthcare sector. This repository contains the API implementation of **RAG (Retrieval-Augmented Generation)**, which facilitates real-time detection of health-related misinformation by combining document retrieval with natural language generation.

## RAG Overview
**RAG (Retrieval-Augmented Generation)** is a hybrid model that enhances traditional NLP systems by:
- **Retrieving relevant data** from credible health sources in real-time.
- **Generating contextually accurate responses** based on retrieved information.
- **Continuously learning** from new data to remain up-to-date on emerging health trends.

### Data Sources
The RAG API pulls health-related data from the following trusted sources:
- **CDC (Centers for Disease Control and Prevention)**
- **NHS (National Health Service)**
- **MedlinePlus**
- **STAT News**
- **MedPage Today**
- **WebMD**
- **News Medical**

## Code Structure
The API is modular, ensuring separation of concerns between retrieval, generation, and API routing.

```plaintext
rag-api/
├── Backend/                   # Backend logic for data retrieval and generation
|    ├── retriever.py          # Handles document retrieval from external sources
|    ├── generator.py          # Manages text generation using the RAG model
|    ├── server.py             # Hosts the Flask API and manages incoming requests
|    └── api/
|         └── rag_api.py       # Main API endpoints for RAG interactions
└── models/                    # Contains model definitions and training scripts
     ├── rag_model.py          # RAG model architecture
     └── training.py           # Script for fine-tuning the model on new data
