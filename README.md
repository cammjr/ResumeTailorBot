# Resume Tailor Bot 🤵

A Gradio-powered web application that tailors a user-provided resume to a specific job posting, leveraging OpenAI function calling for structured metadata extraction and GPT-4 for content refinement.

## Live Demo

> **Note:** This URL is temporary (up to ~72 hours).
>
> https://YOUR-GRADIO-SHARE-LINK.gradio.app

## Features

- **Step-by-step workflow**: Guide users to paste their resume and job posting in sequence.
- **Function-calling**: Extracts company name and job title reliably via OpenAI JSON schema.
- **Tailoring**: Reorders and rewrites resume sections to align with the job description.
- **Download**: Optionally exports the tailored resume as a `.docx` file.

## Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/ResumeTailorBot.git
cd ResumeTailorBot

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate   # Windows

# Install dependencies
pip install -r requirements.txt
```

## Editing the `.env` File

1. Copy the example file:
   ```bash
   cp .env.example .env
   ```
2. Open `.env` in your favorite text editor:
   ```bash
   nano .env   # or code .env / vim .env / notepad .env
   ```
3. Set your OpenAI API key:
   ```ini
   OPENAI_API_KEY=sk-...your-secret-key...
   ```
4. Save and close the editor.

> **Security**: Never commit your `.env` file (with real secrets) to source control. Use `.env.example` for reference.

## Usage

1. Ensure `.env` is configured (see above).
2. Run the app with public sharing enabled:
   ```bash
   python ResumeBot.py --share
   ```
3. Open the printed URL in your browser, paste your resume and job posting, and follow the prompts.

## Environment Variables

- **OPENAI_API_KEY**: Your OpenAI API key (set in `.env`).

## Project Structure

```
ResumeTailorBot/
├── ResumeBot.py         # Main Gradio application
├── requirements.txt     # Python dependencies
├── .env.example         # Sample environment file (no secrets)
└── README.md            # This documentation
```

## Deployment

- **Local demo**: `python ResumeBot.py --share` (free, temporary tunnel)
- **Hugging Face Spaces**: Push repo and configure as a Gradio space.
- **Docker**: Build and run on any cloud VM or PaaS.

## Contributing

Feel free to open issues or PRs to improve the bot—for example, adding authentication or extra tailoring features.

## License

[MIT](LICENSE)
