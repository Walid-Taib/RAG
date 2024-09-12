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


## Built With
The following frameworks and libraries power the API:

- **Flask** - Web framework for hosting the API
- **MongoDB** - Database for storing retrieved documents and metadata
- **Hugging Face Transformers** - Pre-trained models for NLP tasks
- **ElasticSearch** - Fast, scalable document retrieval

## Installation
To run the API locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/rag-api.git
    cd rag-api
    ```

2. Set up the backend:
   Navigate to the `Backend/` directory and install the required dependencies:
    ```bash
    cd Backend
    pip install -r requirements.txt
    ```

3. Set up the model:
   Either download a pre-trained RAG model or fine-tune one using the provided scripts in the `models/` directory.

## Running the API
To start the API server, run the following command from the `Backend/` directory:
```bash
python server.py

