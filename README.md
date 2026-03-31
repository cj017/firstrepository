# WhatsApp AI Agent

This repository contains a Python-based AI agent for WhatsApp that can be trained on custom data.

## Features

- WhatsApp integration via Twilio
- AI responses using OpenAI GPT or locally trained models
- Conversation history for context
- Custom model training capabilities

## Setup

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Configure environment variables:**
   - Copy `.env.example` to `.env`
   - Fill in your Twilio and OpenAI credentials

3. **Set up Twilio WhatsApp:**
   - Create a Twilio account
   - Enable WhatsApp sandbox
   - Set webhook URL to `https://your-domain.com/whatsapp`

## Usage

### Using OpenAI (Cloud)
Run the main app:
```bash
python app.py
```

### Training Custom Model
1. Edit `train_model.py` with your training data
2. Run training:
   ```bash
   python train_model.py
   ```

3. Test locally:
   ```bash
   python local_chatbot.py
   ```

### Deploy
- Use ngrok for local testing: `ngrok http 5000`
- Deploy to Heroku, AWS, or similar for production

## Training Your AI Model

To train the AI on custom data:
1. Add your conversation examples to the `training_data` list in `train_model.py`
2. Run the training script
3. The trained model will be saved in `./whatsapp_model`
4. Update `app.py` to use the local model instead of OpenAI

## Requirements

- Python 3.8+
- Twilio account
- OpenAI API key (optional, for cloud AI)
- GPU recommended for training (optional)
