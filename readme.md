# Learn about git and Git-hub
# How to configure your openai api key and use your model inside python 
``` python
 from openai import OPenai
 from dotenv import load_dotenv
 import os

 load_dotenv()
openai_api_key = os.getenv("OPENAI_API_KEY")