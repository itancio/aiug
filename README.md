# Getting Started


## Open your favorite IDE like VSCode
Using macOS Sonoma (Version 14.5)

## Setting up Virtual Environment
To create a virtual environment, Python supplies a built in venv module which provides the basic functionality needed for the virtual environment. Running the command below will create a virtual environment named "openai-env" inside the current folder you have selected in your terminal / command line:

```bash
python -m venv openai-env
```

Then activate using this cmd:
```bash
source openai-env/bin/activate
```

## Install the OpenAI Python library
```bash
pip install --upgrade openai
```

## Set up your API key for this project
[Source](https://platform.openai.com/docs/quickstart?context=python)
If you only want your API key to be accessible to a single project, you can create a local .env file which contains the API key and then explicitly use that API key with the Python code shown in the steps to come.

Start by going to the project folder you want to create the .env file in.

In order for your .env file to be ignored by version control, create a .gitignore file in the root of your project directory. Add a line with .env on it which will make sure your API key or other secrets are not accidentally shared via version control.

Once you create the .gitignore and .env files using the terminal or an integrated development environment (IDE), copy your secret API key and set it as the OPENAI_API_KEY in your .env file. If you haven't created a secret key yet, you can do so on the API key page.

The .env file should look like the following:
```bash
# Once you add your API key below, make sure to not share it with anyone! The API key should remain private.

OPENAI_API_KEY=123EnterAPIKey
```

Go to the directory where you want to put your secret key.
Go to the project directory: sessions > notebooks > ai_foundations.ipynb.
The API key can be imported by running the following command:

```bash
from openai import OpenAI

client = OpenAI()
# defaults to getting the key using os.environ.get("OPENAI_API_KEY")
# if you saved the key under a different environment variable name, you can do something like:
# client = OpenAI(
#   api_key=os.environ.get("CUSTOM_ENV_NAME"),
# )
```

To start, go to the project directory sessions > session_1 > notebooks > ai_foundations.ipynb and use the README file there to follow along with the tutorials.

SESSION 1: Foundations of AI applications with OPEN AI
SESSION 2: building agentic AI workflows for complex tasks
SESSION 3: Accelerating software development, testing and maintenance with AI
SESSION 4: Building on open-source AI with Hugging Face
SESSION 5: Optimize AI deployment across multiple devices
SESSION 6: Building no-code AI workflows
SESSION 7: Enhance model performance with OpenAI's fine tuning API

