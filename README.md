# Ollama test

## Prepare Ollama and Llama
1. Download and install Ollama for Windows
https://ollama.com/download

2. Open command prompt and check models available
```
ollama list
```

3. Install llama3.2:1b model for chat

```
ollama run llama3.2:1b
```

3. Chat with model via command line
```
ollama
```
Choose "Chat with model"

## Chat with model via Gradio UI

1. Prepare app project
Create folder for project e.g. chat-app  
Open folder in VS Code  

2. Create and activate Python virtual environment
```
python -m venv .venv    
.venv\Scripts\activate    
pip install --upgrade gradio
pip install openai
```

3. Create app.py file with following code:  

```
import gradio as gr

gr.load_chat("http://localhost:11434/v1/", model="llama3.2", token="***").launch()

```

## Run application  
```
python app.py
```

Running on local URL: http://127.0.0.1:7860  
