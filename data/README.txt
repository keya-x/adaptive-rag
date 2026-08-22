RETRIEVAL ARTIFACTS
===================

Project:
Cost-Aware Adaptive RAG

Created by:
Notebook 1 - 01_data_and_retrieval.ipynb

Dataset:
hotpotqa/hotpot_qa
Configuration:
distractor

Embedding model:
BAAI/bge-small-en-v1.5

Corpus:
- Paragraph-level documents
- Deduplicated using SHA1(title + normalized paragraph text)
- Total documents: 62933

Splits:
- Controller train: 5000
- Controller validation: 1000
- Final evaluation: 1000

Retrieval:
- BM25 top-k: 5
- Dense retrieval top-k: 10
- Dense embedding dimension: 384

Files:
- corpus.parquet
    Global paragraph retrieval corpus.

- bm25.pkl
    BM25 index and tokenizer state.

- dense_embeddings.npy
    Normalized BGE paragraph embeddings.

- faiss.index
    FAISS IndexFlatIP dense retrieval index.

- controller_train.parquet
    Controller-training questions with document mappings.

- controller_validation.parquet
    Controller-validation questions with document mappings.

- final_test.parquet
    Held-out final evaluation questions with document mappings.

- corpus_doc_mapping.parquet
    Additional paragraph metadata and source-example mapping.

- retrieval_config.json
    Exact configuration and runtime metadata.

- corpus_stats.json
    Corpus and split statistics.