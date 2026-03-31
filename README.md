# Google GenAI

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

A collection of experiments and scripts using Google AI Studio and Google’s generative AI models to explore text, code, multimodal generation, and API-driven workflows.

### 💻 Setup and Configuration

1. **Create the conda environment:**
   
   ```bash
   conda create -n google-ai python=3.10 -y
   ```

2. **Activate the environment:**
   
   ```bash
   conda activate google-ai
   ```

3. **Install the required dependencies:**
   
   ```bash
   pip install google-genai
   ```

4. **Install supporting packages (optional but recommended):**
   
   ```bash
   pip install python-dotenv requests
   ```

5. **Set API key from Google AI (Gemini):**
   
   ```bash
   setx GOOGLE_API_KEY "your_api_key_here"
   ```
   
   To verify:
   
   ```bash
   echo %GOOGLE_API_KEY%
   ```

6. **Test your setup:**
   
   ```python
   from dotenv import load_dotenv
   import os
   from google import genai
   
   load_dotenv()
   client = genai.Client(api_key=os.getenv("GOOGLE_API_KEY"))
   print(os.getenv("GOOGLE_API_KEY"))
   
   response = client.models.generate_content(
       model="gemini-2.5-flash",
       contents="Hello!"
   )
   
   print(response.text)
   ```

7. **Verify Installation**
   
   If no errors appear, then you're fully set up.
