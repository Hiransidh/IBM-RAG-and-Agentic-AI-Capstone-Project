# IBM RAG and Agentic AI Professional Certificate

Labs and hands-on projects completed as part of the **[IBM RAG and Agentic AI Professional Certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai)** on Coursera.

This repository documents the practical work from a four-module advanced program covering Retrieval-Augmented Generation (RAG), multimodal AI, autonomous agents, and the Model Context Protocol (MCP). It is organized by module and lesson so that notebooks, generated outputs, and supporting assets remain easy to find as the project grows.

## About the Program

> Build real-world AI with RAG and agentic AI.

The certificate develops the skills needed to design sophisticated, context-aware generative AI applications. The curriculum spans the modern generative AI engineering stack, including:

- Prompt engineering and structured output generation
- Unstructured and multimodal data processing
- Retrieval-Augmented Generation pipelines
- Tool use and autonomous agent workflows
- Multi-agent orchestration
- Model Context Protocol (MCP) servers and tools

## Modules

### Module 1 — Generative AI and Structured Extraction

#### M1L1 · Extract Structured JSON from Unstructured Text — Completed

Uses a large language model (LLM) to parse raw restaurant descriptions from a California culinary map into structured JSON. The lab demonstrates prompt engineering for reliable, schema-constrained output and includes:

- A Jupyter notebook containing the lab implementation
- Structured data for 210 restaurant descriptions generated from unstructured text
- Pydantic-based validation and automatic JSON repair for malformed model responses
- A supporting image illustrating the processing flow

**Lab files**

- [Structure Text and Multimodal Data with LLMs.ipynb](./M1L1/Structure%20Text%20and%20Multimodal%20Data%20with%20LLMs.ipynb)
- [structured_restaurant_data.json](./M1L1/structured_restaurant_data.json)
- [M1L1_structure_for_loop.png](./M1L1/M1L1_structure_for_loop.png)

**Concepts demonstrated**

- Loading and splitting unstructured restaurant descriptions
- Calling the IBM Granite 4H Small model through the IBM watsonx.ai SDK
- One-shot prompt engineering for structured extraction
- Validating model responses against a defined schema
- Repairing invalid JSON responses before saving the final dataset
- Assigning stable `itemId` values to the structured records

**Dependencies**

```text
numpy==2.3.4
matplotlib==3.10.7
ibm-watsonx-ai==1.4.7
```

#### M1L2 · Process Multimodal Data with LLMs — Completed

Uses multimodal foundation models to generate descriptive captions for food images and enrich existing recipe and user-review datasets. This lab connects visual information with structured text so it can be used in a unified, machine-readable knowledge base.

- Generated image descriptions for 109 food recipe records
- Added image captions to 10 user review records
- Used recipe names and review text as context for more relevant captions
- Preserved the original structured data while adding multimodal fields

**Lab files**

- [M1L2_Process_Multimodal_Data_with_LLMs.ipynb](./M1L2/M1L2_Process_Multimodal_Data_with_LLMs.ipynb)
- [augmented_food_recipe.json](./M1L2/augmented_food_recipe.json)
- [augmented_user_review.json](./M1L2/augmented_user_review.json)
- [M1L2_caption_all_recipes.jpg.png](./M1L2/M1L2_caption_all_recipes.jpg.png)

**Concepts demonstrated**

- Loading recipe and user-visit JSON data containing image references
- Calling a vision-capable LLM through the IBM watsonx.ai SDK
- Designing image-caption prompts with recipe and review context
- Downloading and processing images referenced by URLs
- Adding `image_description` and `image_captions` fields to structured records
- Using retry handling for image requests before saving enriched JSON datasets

### Module 2 — Retrieval-Augmented Generation

This module covers the foundations and implementation of RAG systems, including document ingestion, chunking, embeddings, vector search, retrieval, and grounded generation.

### Module 3 — Autonomous and Multi-Agent AI

This module explores agentic workflows, tool calling, planning, memory, and collaboration between specialized AI agents.

### Module 4 — Model Context Protocol and Agent Orchestration

This module focuses on MCP-based tool and context orchestration, enabling agents to interact with external data sources and services through standardized interfaces.

## Repository Structure

```text
.
├── M1L1/
│   ├── Structure Text and Multimodal Data with LLMs.ipynb
│   ├── structured_restaurant_data.json
│   └── M1L1_structure_for_loop.png
├── M1L2/
│   ├── M1L2_Process_Multimodal_Data_with_LLMs.ipynb
│   ├── augmented_food_recipe.json
│   ├── augmented_user_review.json
│   └── M1L2_caption_all_recipes.jpg.png
├── .gitignore
└── README.md
```

Each lesson follows the `M<module>L<lesson>` naming convention. New notebooks, outputs, and supporting resources can be added to the corresponding lesson directory without changing the overall organization.

## Technologies and Concepts

- Python
- Jupyter Notebooks
- Large language models (LLMs)
- Prompt engineering
- Structured JSON extraction
- Retrieval-Augmented Generation (RAG)
- Embeddings and vector databases
- AI agents and multi-agent systems
- Model Context Protocol (MCP)

## Getting Started

1. Clone or download this repository.
2. Open the project in Jupyter Notebook, JupyterLab, or Visual Studio Code.
3. Open the notebook for the lesson you want to explore.
4. Install the dependencies required by that notebook.
5. Run the notebook cells from top to bottom.

Notebook-specific setup instructions and dependencies are documented within each lab where applicable.

## Learning Outcomes

By working through the labs in this repository, you will build practical experience with:

- Converting unstructured information into reliable, machine-readable data
- Designing prompts for consistent structured output
- Building systems that retrieve relevant context before generating responses
- Connecting LLMs to tools, APIs, and external data
- Designing autonomous and collaborative agent workflows
- Using MCP to standardize context and tool access

## License

This repository contains educational work created while completing the IBM RAG and Agentic AI Professional Certificate. Refer to the original course materials and platform terms for the licensing of course-provided content and assets.