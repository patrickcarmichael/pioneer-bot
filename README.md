# NamaBot

A Discord bot that learns to mimic *ficticious Brooklyn autistic man*—the guy who won’t shut up about obscure glitch techno and that one “life-changing” trip to Germany—from his iMessage and Discord diatribes.

## Overview

NamaBot combs through Chaty Snob’s iMessage and Discord logs to build a language model that captures his “you wouldn’t get this microgenre” swagger. It’s got basic Markov chains (for that jerky, lo-fi feel) and fine-tuned LLMs (for when you want it to lecture you on Berlin’s superiority for hours).

## Features

- Extracts iMessage rants about “plebs who don’t get minimal techno”
- Scrapes Discord sermons on that one night at Berghain in 2019
- Cleans up his nonstop snobbery (good luck with that)
- Trains a model to churn out messages that ooze niche elitism
- Deploys a Discord bot that’s part rare-Vinyl nerd, part Berlin evangelist
- Pick your flavor: Markov (clunky like a bad remix) or LLM (smug like he is)

## Prerequisites

- Python 3.8+ (he’d scoff at anything less “cutting-edge”)
- Discord dev account (too mainstream for him to bother with)
- iMessage chat.db (macOS—where he types “Berlin > your life”)
- Discord API token (he’d lose it critiquing your playlist)
- Chat logs of him flexing his niche cred

### Dependencies

```
discord.py>=2.0.0  # For bot antics
pandas>=1.0.0      # To sort his pretentious data
sqlite3            # For iMessage’s retro charm
markovify>=0.9.0   # Stilted like his obscure beats
transformers>=4.18.0  # For that “I’m above you” tone
python-dotenv>=0.19.0  # To hide keys he’d scoff at hiding
```

## Installation

1. Clone this thing (he’d call git “too corporate”):

```bash
git clone https://github.com/yourusername/NamaBot.git
cd /Users/patrick/code/NamaBot
```

2. Set up a virtual environment (he’d say it’s “not authentic”):

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

3. Install the stuff (faster than his Berlin story):

```bash
pip install -r requirements.txt
```

## Configuration

1. Add a `.env` file with your Discord token (he’d judge your security):

```
DISCORD_TOKEN=your_discord_bot_token
```

2. Tweak `config.py` to track Berlin Beat Snob:

```python
# Target info
TARGET_CONTACT = "+1234567890"  # His phone, still buzzing from Berlin flashbacks
TARGET_DISCORD_USER_ID = "123456789012345678"  # His ID, king of #niche-beats

# Paths
IMESSAGE_DB_PATH = "/Users/patrick/Library/Messages/chat.db"
OUTPUT_DIR = "/Users/patrick/code/NamaBot/data"
MODEL_PATH = "/Users/patrick/code/NamaBot/model.json"
```

## Usage

### Step 1: Extract the Elitism

#### From iMessage:

```bash
python extract_imessage.py
```

#### From Discord:

```bash
python extract_discord.py
```

Brace for “Berlin’s underground scene changed me” on repeat.

### Step 2: Process and Train

```bash
python train_model.py
```

Turns his snobbery into a bot that name-drops Aphex Twin nonstop.

### Step 3: Unleash the Snob

```bash
python bot.py
```

Watch it gatekeep your server with rare B-sides and Berlin lore.

## Project Structure

```
/Users/patrick/code/NamaBot/
├── .env                  # Secrets he’d deem “too mainstream”
├── config.py             # Settings he’d call “basic”
├── requirements.txt      # Tools he’d sneer at
├── README.md             # This file he’d skim for “Berlin”
├── extract_imessage.py   # His iPhone techno manifestos
├── extract_discord.py    # His Discord niche flexes
├── process_data.py       # Filtering his endless takes
├── train_model.py        # Building his smug avatar
├── bot.py                # The snobbery lives
├── data/                 # His essence in CSV
│   ├── imessage_data.csv  # “You wouldn’t get this track”
│   └── discord_data.csv   # 6000 words on Berlin’s grit
└── models/               # His brain, preserved
    ├── markov_model.json  # Choppy like his rare cuts
    └── llm_model/         # Polished like his ego
```

## Advanced Usage

### Fine-tuning the Pretension

For peak “you’ve never heard of this label” vibes, fine-tune an LLM:

```bash
python train_llm.py
```

Dumps a model in `models/llm_model/`.

### Switching to Elite Mode

Make the bot as insufferable as he is:

```python
# In bot.py
USE_LLM = True  # False for that “glitchy demo” Markov vibe
```

## Troubleshooting

### Common Snags

#### iMessage Blocks You
```
Error: unable to open database file
```
Fix: Give Terminal Full Disk Access. He’d blame “uncultured tech.”

#### Discord Says “Enough”
```
discord.errors.HTTPException: 429 Too Many Requests
```
Fix: Ease up—he’d say the API “can’t handle true art.”

## License

MIT License—open like his Berlin tales, but less tedious. See LICENSE.

## Disclaimer

This is _entirely ficticious_ and **definitely** not based on a real person in ravesNYC.
