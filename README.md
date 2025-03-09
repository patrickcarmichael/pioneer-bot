# Nama Larjug

A Discord bot that learns to mimic a specific person's communication style from iMessage and Discord chat history.

## Overview

PersonaBot analyzes conversation data from iMessage and Discord to build a language model that generates messages in the style of a specific person. This project uses natural language processing techniques ranging from simple Markov chains to fine-tuned language models.

## Features

- Extract conversation data from iMessage database
- Extract conversation data from Discord channels
- Process and clean message data
- Train language models on the conversation corpus
- Deploy a Discord bot that responds in the learned communication style
- Support for both basic (Markov chain) and advanced (fine-tuned LLM) approaches

## Prerequisites

- Python 3.8+
- Discord account with developer access
- Access to iMessage chat.db (macOS)
- Discord API token
- Direct message history with the person you want to mimic

### Dependencies

```
discord.py>=2.0.0
pandas>=1.0.0
sqlite3
markovify>=0.9.0
transformers>=4.18.0 (for LLM approach)
python-dotenv>=0.19.0
```

## Installation

1. Clone this repository:

```bash
git clone https://github.com/yourusername/personabot.git
cd /Users/patrick/code/personabot
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

## Configuration

1. Create a `.env` file in the project root with your Discord token:

```
DISCORD_TOKEN=your_discord_bot_token
```

2. Configure extraction parameters in `config.py`:

```python
# Target contact information
TARGET_CONTACT = "+1234567890"  # Phone number for iMessage
TARGET_DISCORD_USER_ID = "123456789012345678"  # Discord user ID

# Paths
IMESSAGE_DB_PATH = "/Users/patrick/Library/Messages/chat.db"
OUTPUT_DIR = "/Users/patrick/code/personabot/data"
MODEL_PATH = "/Users/patrick/code/personabot/model.json"
```

## Usage

### Step 1: Extract Data

#### From iMessage:

```bash
python extract_imessage.py
```

#### From Discord:

```bash
python extract_discord.py
```

### Step 2: Process Data and Train Model

```bash
python train_model.py
```

### Step 3: Run the Bot

```bash
python bot.py
```

## Project Structure

```
/Users/patrick/code/personabot/
├── .env                  # Environment variables (Discord token)
├── config.py             # Configuration settings
├── requirements.txt      # Project dependencies
├── README.md             # This file
├── extract_imessage.py   # Script to extract iMessage data
├── extract_discord.py    # Script to extract Discord data
├── process_data.py       # Data cleaning and processing
├── train_model.py        # Model training (Markov or LLM)
├── bot.py                # Discord bot implementation
├── data/                 # Directory for storing extracted messages
│   ├── imessage_data.csv
│   └── discord_data.csv
└── models/               # Directory for trained models
    ├── markov_model.json
    └── llm_model/        # For the fine-tuned LLM approach
```

## Advanced Usage

### Fine-tuning a Language Model

For more realistic and contextual responses, you can fine-tune a pre-trained language model instead of using Markov chains:

```bash
python train_llm.py
```

This will create a fine-tuned model in the `models/llm_model/` directory.

### Using the Fine-tuned Model

Update your bot configuration to use the fine-tuned model:

```python
# In bot.py
USE_LLM = True  # Set to False to use Markov chain instead
```

## Troubleshooting

### Common Issues

#### Cannot access iMessage database
```
Error: unable to open database file
```
Solution: Ensure Terminal has Full Disk Access in System Preferences → Privacy & Security.

#### Discord API rate limiting
```
discord.errors.HTTPException: 429 Too Many Requests
```
Solution: Implement rate limiting in your bot code or reduce frequency of requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This tool is for educational and personal use only. The creators are not responsible for any misuse or violation of Discord's Terms of Service or any applicable laws regarding privacy and impersonation.
