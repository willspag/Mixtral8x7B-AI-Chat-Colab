# Mixtral8x7B-AI-Chat-Colab
Download, Initialization, Tooling, and Chat Session Logic of Mistal AI's Mixtral8x7B "Mixtral of Experts" model in Google Colab

[![Run in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/willspag/Mixtral8x7B-AI-Chat-Colab/blob/main/Mixtral8x7B_AI_Chat_with_Tools.ipynb)

## This notebook downloads and initializes Mistal AI's Mixtral8x7B [Mixtral of Experts](https://mistral.ai/news/mixtral-of-experts/) using the [Huggingface transformers](https://huggingface.co/docs/transformers/index) package along with facilitating Tool Usage and Chat Session Logic.

The code is based on this [Pinecone Tutorial](https://www.pinecone.io/learn/mixtral-8x7b/) and extends it to include additional inference/memory improvements (4-bit/8-bit quantization and Flash Attention 2) along with full multi-step chat logic. Please check out their tutorial for a step-by-step walkthrough on the implementation.

### Tools

- "Calculator" - Enables Mixtral AI Assistant to perform math calculations by providing python code which is then run executed using exec() - **WARNING* Using exec() to execute arbitrary Python code can be dangerous, as it can execute any Python command. This might lead to security vulnerabilities, especially in a web-based environment like Google Colab. This notebook does not currently apply any sanitzation, filtering, or other safety measures to the code generated by the Mixtral model before code execution, so please be cautious and use at your own risk.**
- "Search" - Enables Mixtral AI Assistant to Search the web for real-time information using DuckDuckGo
