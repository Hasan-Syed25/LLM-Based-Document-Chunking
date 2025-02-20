# LLM-Based Document Chunking Notebook

## Overview

This repository contains a Jupyter Notebook that demonstrates an advanced approach to document chunking using Large Language Models (LLMs). Traditional chunking methods often split clauses or headings into multiple segments, leading to incomplete context during retrieval and increasing the risk of hallucinations in LLM outputs. This notebook addresses these challenges by ensuring that each clause remains intact, preserving the document's logical structure and cross-references.

## Features

- **Whole Clause Integrity:** Maintains entire clauses in single chunks to preserve context.
- **Versatile Chunking:** Supports documents with or without a Table of Contents (ToC).
- **Cross-Reference Preservation:** Captures and retains references between clauses for enhanced retrieval accuracy.

## Requirements

- Python 3.8 or higher
- Jupyter Notebook
- OpenAI API Key
- Required Python packages:
  - `openai`
  - `python-docx`
  - `nltk`
  - `json`
  - `os`
  - `re`

## Usage

1. **Launch Jupyter Notebook:**

   ```bash
   jupyter notebook
   ```

2. **Open the Notebook:**

   In the Jupyter interface, open `LLM_Document_Chunking.ipynb`.

3. **Configure Parameters:**

   Inside the notebook, set the following parameters:
   - `input_path`: Path to the input DOCX file.
   - `output_dir`: Directory to save the output files.
   - `api_key`: Your OpenAI API key.
   - `endpoint`: Azure OpenAI API endpoint (if applicable).
   - `deployment_name`: Name of the GPT model deployment.

4. **Run the Notebook:**

   Execute the cells sequentially to process the document and extract structured content.

## Example

```python
input_path = 'path/to/your/document.docx'
output_dir = 'path/to/output/directory'
api_key = 'your-openai-api-key'
endpoint = 'https://api.openai.com/v1/engines/davinci-codex/completions'
deployment_name = 'your-deployment-name'

# Run the processing function
process_document(input_path, output_dir, api_key, endpoint, deployment_name)
``` 
