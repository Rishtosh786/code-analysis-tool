
# Code Analysis and Improvement Tool

## Introduction

The Code Analysis and Improvement Tool is a Python-based utility designed to streamline the code review, optimization, and quality assurance processes. This tool integrates ChatGPT (versions 3.5) and GitHub, providing automated suggestions for codebase improvements.

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Configuration](#configuration)
4. [Token Management](#token-management)
5. [GitHub Repository Fetching](#github-repository-fetching)
6. [Codebase Analysis with LLMs](#codebase-analysis-with-llms)
7. [Model Analysis and Suggestions](#model-analysis-and-suggestions)
8. [Documentation and Reporting](#documentation-and-reporting)
9. [Contributing](#contributing)
10. [License](#license)

## Installation
1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/Rishtosh786/code-analysis-tool.git
    ```
2. Navigate to the tool's directory:
    ```bash
    cd code-analysis-tool
    ```
3. Install the required libraries:
    ```bash
    pip install PyGithub
    pip install openai
    pip install python-dotenv
    ```
## Usage
Run the tool by executing the main script:
```bash
python code_analysis_tool.py
```

## Configuration
1. Create a file named '.env' in your project's root directory.

2. Add the following lines to the '.env' file:
 ```bash
 GITHUB_REPOSITORY_URL=your_username/your_repository
 GITHUB_ACCESS_TOKEN=your_github_access_token

Replace 'your_username/your_repository' with the actual GitHub repository URL and set 'your_github_access_token' with your GitHub access token.

 LOCAL_PATH=/path/to/your/local/directory
 
Replace '/path/to/your/local/directory' with the desired local path. 

CHATGPT_ACCESS_TOKEN=your_chatgpt_access_token

Replace your_chatgpt_access_token with the actual ChatGPT access token.
```
3. With this setup, you can use the 'python-dotenv' library in your script to load the variables from the '.env' file.
```bash
pip install python-dotenv

import os
from dotenv import load_dotenv

# Load environment variables from .env file
load_dotenv()

# GitHub configuration
github_repository_url = os.getenv("GITHUB_REPOSITORY_URL")
github_access_token = os.getenv("GITHUB_ACCESS_TOKEN")

# Local configuration
local_path = os.getenv("LOCAL_PATH")

# ChatGPT configuration
chatgpt_token = os.getenv("CHATGPT_ACCESS_TOKEN")
```
## Token Management

GitHub Token:
To use the tool, generate a GitHub token with the necessary permissions (repo, read:user). Set this token as the GITHUB_ACCESS_TOKEN environment variable.

ChatGPT Token:
Obtain a ChatGPT token from OpenAI and set it as the CHATGPT_ACCESS_TOKEN environment variable.


## GitHub Repository Fetching
The tool fetches code from the specified GitHub repository using the GitHub API. Ensure the repository is accessible and the token has the necessary permissions.

```bash
# Function to authenticate and get GitHub repository details
def get_repository_details(repo_url, github_token):

# Function to fetch Python code from a GitHub repository
def fetch_python_code_from_repository(repo, local_path):

# Function to find Python files in a directory
def find_python_files(directory):
```

## Codebase Analysis with LLMs
The tool integrates ChatGPT for code analysis. It provides suggestions for code improvement, optimization, test case development, and bug identification.
```bash
# Function to analyze Python code using ChatGPT
def analyze_code_with_chatgpt(code_snippet, chatgpt_token):
```

## Model Analysis and Suggestions
The tool analyzes the code and provides suggestions for:

Code Improvement
Code Optimization
Test Case Development
Bug Identification and Resolution


## Documentation and Reporting
Review the output for actionable insights and recommendations.

## Contributing
Contributions to the tool are welcome! Fork the repository, make your changes, and submit a pull request.

## License
This tool is licensed under the MIT License.


