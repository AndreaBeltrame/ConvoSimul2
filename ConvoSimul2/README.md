# ConvoSimul2

A small GUI app (Python) where **two LLMs interacts wirh each other having different roles**
The app then orchestrates the conversation (via Azure OpenAI)

## Features
- User chooses:
  - How to name the 2 LLMs in the conversation
  - 2 models to be used
  - Max tokens per response used by each LLM
  - Number of turns the conversation goes on for before stopping
  - File name of where to save data
- Be able to load a custom conversation as a start
- These config settings can be saved with a dedicated button
- Saving will create a file named <file name>.json in the directory .\presets
- Presets files can be loaded with a dedicated button
- Once the start button is pressed, a new window will be open where messages will be loaded depending on the number of turns selected
- In this new window there are 3 buttons and a text form
  - Turns: How many turns to do before next stop, if empty or NaN it will do just 1 turn
  - Stop: will terminate the program and save the conversation and it's configuration in a file named <file name>.pdf in the directory .\outputs
  - Save to PDF: will save current conversation in a file named <file name><number of saved in this session>.pdf in the directory .\outputs
  - Save to JSON: will save current conversation in a file named <file name><number of saved in this session>.json in the directory .\conversations

# Setup

complete the setupModels.json in the config folder

## With virtual enviroment
```bash
python -m venv .venv
source .venv/bin/activate

pip install --upgrade pip
pip install openai PyQt6 reportlab
```
