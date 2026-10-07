
### Login into 
`platform.openai.com`

#### Add Credits 
 - In billing : Minimum $5
### Once Credit added , Added API Key 
 - To be used for querying the LLM

---
1. Create python env
 `python -m venv venv`
2. activate the env
 - Powershell : `.venv\Scripts\Activate.ps1`
 - LInux/Mac: `source .venv/bin/activate`

 3. Install openai:  `pip install openai`
 4. Save the dependency : `pip freeze > requirements.txt`

---
 ### Environment Variables (.env files)

If you are trying to manage configuration settings or secret keys (like API keys) without hardcoding them into your scripts, you use a .env file.
1. Create a file named exactly `.env` in your project root directory.
2. Add your secrets inside it:
```env
OPEN_API_KEY=your_secret_key_here
```
3. Install the loader package: `pip install python-dotenv`
4. Access the variables in Python 
```python
import os
from dotenv import load_dotenv

# Load the variables from the .env file
load_dotenv()
# Access them using os.environ
api_key = os.getenv("API_KEY")
print(api_key)
```

---
### Python code to call Open API
```python
from openai import OpenAI
import os
from dotenv import load_dotenv

load_dotenv()


client = OpenAI()
response=client.chat.completions.create(
    model="gpt-4o",
    messages = [
        { "role": "user","content": "Hi There!!" }
    ]
)
print(response.choices[0].message.content)
```
