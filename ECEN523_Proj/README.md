### README

# Research Assistant with Page-Level Embeddings and Dual RAG Pipelines

#### By Aly Khater and Aaron Pluemer

## Description

This project implements a research assistant that utilizes page-by-page embeddings and two Retrieval Augmented Generation (RAG) pipelines to provide efficient and precise retrieval. While many embedding implementations perform document-level or paragraph-level embeddings, the assistant is designed for live research assistance, prioritizing a balance between retrieval specificity and speed. The assistant uses OpenAI's GPT-3.5 for generative responses, allowing for coherence and accuracy.

## Features

- **Page-Level Embeddings:** Documents are processed and embedded page by page, enabling a faster and more efficient retrieval compared to paragraph-level approaches. This also provides additional context that may be useful for receiving a more accurate response.
- **Dual RAG Pipelines:** Two separate RAG pipelines are utilized, one for retrieving information from background materials and another for accessing reference documents.
- **Optimized Retrieval:** The system is tuned to provide a balance between specific and fast retrieval, catering to the demands of live research assistance.
- **Google Drive Integration:** Research materials are stored in a mounted Google Drive, providing a scalable and accessible storage solution. The Background folder contains research materials for background knowledge. The Reference folder contains research materials on how to advance the the writing.
- **OpenAI GPT-3.5 Integration:** The GPT-3.5 language model is employed to generate informative and contextually relevant responses.

## How to use

**Running the Code**
- Open in Google Colab: Access the notebook in Google Colab.
- Authenticate with Google Drive: Execute the code block that prompts you to authorize access to your Google Drive. This allows the research assistant to access the papers stored in the drive.
- Run All Cells: Sequentially execute all code blocks in the notebook. This initializes the RAG pipelines, loads the necessary models, and prepares the system for continuous interaction.

**Interacting with the Research Assistant**
- Input Box: Upon running all code blocks, an input box will appear at the bottom of the notebook.
- Ask Questions: Type your research questions or prompts into the input box.
- Receive Responses: The research assistant will process your query, retrieve relevant information from the papers in your Google Drive, and generate a relevant response.

**Sample interactions**
- "Give me the definition of the Dropout Layer"
- "Transformers in LLMs"
- "Can you name 2 methods to improve data preprocessing?"
- "Give me a topic sentence for CNNs"

### Modifying the Background and References folders

For the purposes of this demo, 5 papers in the past few years were selected as the references:
- Attention Is All You Need (2017)
- BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding (2019)
- Language Models are Few-Shot Learners (2020)
- An Image Is Worth 16X16 Words: Transformers For Image Recognition At Scale (2021)
- Highly accurate protein structure prediction with AlphaFold (2021)

An additional 18 papers from the decades preceding it were selected as the background. These include:
- Generative Adversarial Nets (2014) 
- Dropout: A Simple Way to Prevent Neural Networks from Overfitting (2014)
- Random Forests (2001)
- Bagging Predictors (1996)
- And many others

All the papers selected are a subset of the **Historical Papers** at https://github.com/aimerou/awesome-ai-papers?tab=readme-ov-file#historical-papers-

The Background and Reference folders can be modified simply by adding or replacing them with other PDF documents. **All other file types in those folders are ignored.**
