# DO-RAG: A Domain-Specific QA Framework Using Knowledge Graph-Enhanced Retrieval-Augmented Generation

## Abstract

Domain-specific QA systems require not just generative fluency but high factual accuracy grounded in structured expert knowledge. While recent Retrieval-Augmented Generation (RAG) frameworks improve context recall, they struggle with integrating heterogeneous data and maintaining reasoning consistency. To address these challenges, we propose DO-RAG, a scalable and customizable hybrid QA framework that integrates multi-level knowledge graph construction with semantic vector retrieval. Our system employs a novel agentic chain-of-thought architecture to extract structured relationships from unstructured, multimodal documents, constructing dynamic knowledge graphs that enhance retrieval precision. At query time, DO-RAG fuses graph and vector retrieval results to generate context-aware responses, followed by hallucination mitigation via grounded refinement. Experimental evaluations in the database and electrical domains show near-perfect recall and over 94% answer relevancy, with DO-RAG outperforming baseline frameworks by up to 33.38%. By combining traceability, adaptability, and performance efficiency, DO-RAG offers a reliable foundation for multi-domain, high-precision QA at scale.


## Key Contributions

- **Agentic, multi-stage KG construction**: We design and implement a hierarchical, agent-based extraction pipeline that processes text, tables, code snippets, and images to automatically build and update a knowledge graph capturing entities, relations, and attributes.

- **Hybrid retrieval fusion**: We develop a unified mechanism that merges graph-based traversal with semantic search at query time, ensuring that all relevant, structurally grounded information informs the LLM’s prompt.

- **Grounded hallucination mitigation**: We introduce a post-generation refinement step that cross-verifies initial LLM outputs against the knowledge graph and iteratively corrects inconsistencies, dramatically reducing factual errors.

- **Plug-and-play modularity**: Our framework accommodates diverse LLMs and retrieval modules, enabling seamless component swapping and straightforward extension to new domains without retraining.

## Performance

Evaluated on expert-curated benchmarks in the database and electrical engineering domains, DO-RAG achieves:
- Near-perfect contextual recall
- Over 94% answer relevancy
- Outperforms existing RAG platforms (FastGPT, TiDB.AI, Dify.AI) by up to 33.38%

## Architecture

The architecture of DO-RAG consists of three main components:

1. **Knowledge Graph Construction Pipeline**
   - Processes multimodal documents (text, tables, code, images)
   - Extracts entities, relations, and attributes
   - Builds a dynamic, multi-level knowledge graph

2. **Hybrid Retrieval System**
   - Combines graph traversal with semantic vector search
   - Assembles context-rich prompts for the LLM

3. **Grounded Generation and Refinement**
   - Generates initial responses based on retrieved context
   - Cross-verifies outputs against the knowledge graph
   - Iteratively corrects inconsistencies and hallucinations

## Applications

DO-RAG provides a scalable, high-precision solution for domain-specific QA across various technical fields, including:
- Database systems
- Electrical engineering
- Other specialized technical domains requiring structured knowledge

## Authors

- David Osei Opoku - Department of Computer Science and Technology, Tsinghua University, Beijing, China
- Ming Sheng - Beijing National Research Center for Information Science and Technology - Tsinghua University, Beijing, China
- Yong Zhang (Corresponding Author) - Beijing National Research Center for Information Science and Technology - Tsinghua University, Beijing, China

## Citation

```
@article{opoku2023dorag,
  title={DO-RAG: A Domain-Specific QA Framework Using Knowledge Graph-Enhanced Retrieval-Augmented Generation},
  author={Opoku, David Osei and Sheng, Ming and Zhang, Yong},
  journal={},
  year={2023},
  publisher={}
}
```
