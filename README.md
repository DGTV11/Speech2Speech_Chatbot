# Speech2Speech Chatbot 
A (hopefully easy-to-use) speech-to-speech chatbot

## Installation
1) Install Python dependencies
```sh
pip install -r requirements.txt
```

2) Install ffmpeg

3) Install the required Ollama models
```sh
ollama pull llama3 mistral openchat phi3 nomic-embed-text
```

## Usage (CLI)
1) Configure Speech2Speech_Chatbot if you have not already done so
```sh
python3 config.py
```

2) Run Speech2Speech_Chatbot
```sh
python3 main.py
```

## Troubleshooting
If you are on Linux and playsound freezes up and doesn't play anything, run the following commands:
```sh
sudo apt-get install libx264-dev libjpeg-dev
sudo apt-get install libgstreamer1.0-dev \
     libgstreamer-plugins-base1.0-dev \
     libgstreamer-plugins-bad1.0-dev \
     gstreamer1.0-plugins-ugly \
     gstreamer1.0-tools \
     gstreamer1.0-gl \
     gstreamer1.0-gtk3
sudo apt-get install gstreamer1.0-qt5
sudo apt-get install gstreamer1.0-pulseaudio
```

## Note
- The code in llm_os is based on the MemGPT codebase [here](https://github.com/cpacker/MemGPT) (some parts are from the codebase, some parts are from the internet)
- The system instructions have been lifted from [here](https://github.com/cpacker/MemGPT/tree/c6325feef6d9d2154c0445e317bcc06a7eb27665/memgpt/prompts) with few edits
- The schema generator has been lifted from [here](https://github.com/cpacker/MemGPT/tree/c6325feef6d9d2154c0445e317bcc06a7eb27665/memgpt/functions/schema_generator.py) with few edits
- The base function set has been lifted from [here](https://github.com/cpacker/MemGPT/tree/c6325feef6d9d2154c0445e317bcc06a7eb27665/memgpt/functions/function_sets/base.py) with few edits

## TODO
- Implement MemGPT architecture
- Allow it to use function-calling to interact with its environment, search the web, use LSA/COT, and perform other actions

## References
<a id="1">[1]</a> 
Charles Packer and Sarah Wooders and Kevin Lin and Vivian Fang and Shishir G. Patil and Ion Stoica and Joseph E. Gonzalez. (2024).
MemGPT: Towards LLMs as Operating Systems.

<a id="2">[2]</a>
Zach Nussbaum and John X. Morris and Brandon Duderstadt and Andriy Mulyar (2024)
Nomic Embed: Training a Reproducible Long Context Text Embedder
