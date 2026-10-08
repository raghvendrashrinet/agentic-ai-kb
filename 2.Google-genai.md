### setup google gemini api
> pip install google-genai
### generate api key in gemini studio
- `.env` add key, Key name should be same as below
  `GEMINI_API_KEY=key`
### Python Code
```python
from google import genai
import os
from dotenv import load_dotenv

load_dotenv()
api_key = os.getenv("GEMINI_API_KEY")
print(api_key)

client = genai.Client(api_key=api_key)

interaction = client.models.generate_content(
    model="gemini-3.5-flash-lite",
    contents="hello gemini hw r u"
)

print(interaction.text)
```
