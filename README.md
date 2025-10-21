# One-Inc-Software-Engineer-I-AI-Agentic-Coding-Assignment
LLM Rephraser
A single-page application (SPA) that uses a Hugging Face-hosted Large Language Model (LLM) to rephrase user input into four distinct writing styles: Professional, Casual, Polite, and Social-media. Built with Gradio for the frontend and Python for the backend, this app runs entirely in Google Colab and supports streaming output and cancellation.

Features
*  Rephrases input into multiple writing styles using an LLM
*  Real-time streaming output (word-by-word)
* Cancel button to interrupt processing
*  Unit and integration tests included
* Docker containerization for backend
* Clean, enterprise-grade UI using Gradio Blocks

Tech Stack
Layer	Technology
Frontend	HTML + JavaScript via Gradio
Backend	Python (no Flask)
LLM	Hugging Face mistralai/Mistral-7B-Instruct-v0.2
Platform	Google Colab
Setup Instructions (Google Colab)
1. Enable GPU: Go to Runtime → Change runtime type → GPU
2. Install dependencies: 
!pip install -q transformers accelerate gradio huggingface_hub
  3. Authenticate with Hugging Face:       
from huggingface_hub import login
login("your_huggingface_token_here")
4. Run the notebook cells to launch the Gradio app.

Testing
Run the following test functions in Colab:

test_prompt_builder()
test_model_response()
test_end_to_end()

All tests validate prompt formatting, model output, and full pipeline integration.

Assumptions
* You have access to the gated Hugging Face model mistralai/Mistral-7B-Instruct-v0.2
* You are running this in a GPU-enabled Colab environment
* You have a valid Hugging Face token with read access
