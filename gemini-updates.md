

# Update packages for google-generativeai

Manually appending packages:
These commands are tricky. 

```bash

# add dependencies
uv add google-genai
uv sync --refresh
uv pip list | grep google-genai
uv lock

# Only if aforementioned add commands do not install the new packages, clean uv cache and Install dependencies
uv cache clean --force
uv pip install google-genai

# since uv add [package-name] also runs uv sync

# Set up GEMINI API API key into a .env file
echo "GEMINI_API_KEY=your-key-here" > .env

```
