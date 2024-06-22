# Comparative Analysis of Llama3 and Gemma:7b using ollama CLI

The ollama CLI tool is crafted to enable smooth integration and interaction with advanced Large Language Models (LLMs) like Llama3 and Gemma:7b directly from your local environment. In this analysis, I leverage the ollama CLI to evaluate how these models handle various prompts, making it a perfect tool for researchers, developers, and enthusiasts keen on delving into the functionalities of cutting-edge language models.

## Features
- **Easy Model Management**: Download and switch between Llama3 and Gemma:7b models with a single command.
- **Local API**: Set up a local server to interact with the models via a RESTful API.
- **Secure and Private**: All processing is done locally on your machine, ensuring data privacy and security.


## YouTube Link
For a visual and detailed explanation, watch my video [here](https://www.youtube.com/watch?v=AjUME0Ev-j0).

## Getting Started

### Prerequisites
Before you begin, ensure you have the following installed:
- Python 3.8 or higher
- pip (Python package installer)

### Installation
To install the ollama CLI, run the following command in your terminal:

```pip install ollama-cli```

### Download and Run a Model

To download and start a model server, use the following command:

```ollama run <model_name>```

Replace ```<model_name>``` with ```llama3``` or ```gemma7b``` to use the respective model.

### Interact with the Model

After the model server is running, you can ask questions or send prompts using curl. For example:


```
curl -X POST -H "Content-Type: application/json" -d '{
    "model": "<model_name>",
    "prompt": "Question",
    "stream": false
}' "http://localhost:11434/api/generate"
```
This command sends a question to the model running locally on your machine.

## API Reference
The ollama CLI exposes a RESTful API to interact with the models. The main endpoint is:

```POST /api/generate```

### Request Parameters
- **model**: The model you want to interact with (llama3 or gemma7b).
- **prompt**: The text prompt or question you want to send to the model.
- **stream**: Whether the response should be streamed (set to false for a single response).

### Response
The API responds with the generated text from the model, based on the input prompt.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Please make sure to update tests as appropriate.

## License
[MIT-License](https://choosealicense.com/licenses/mit/)

