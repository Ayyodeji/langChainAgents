# Langchain Agents - README

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Configuration](#configuration)
- [Usage](#usage)
  - [Running the Application](#running-the-application)
  - [Simulating Conversations](#simulating-conversations)
- [Customizing Agents](#customizing-agents)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Langchain Agents is a Streamlit web application that allows users to simulate conversations with virtual agents. These agents have specific roles, such as CEO, CTO, and Assistant, and can provide responses based on predefined templates and tools.

This README provides detailed instructions on how to set up and use the Langchain Agents application.

## Features

- Simulate conversations with virtual agents.
- Customizable agent templates and responses.
- Integration with external tools for answering user queries.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.6 or higher installed on your system.
- Access to [OpenAI GPT-3](https://beta.openai.com/signup/) (as the code relies on GPT-3 for generating agent responses).
- Access to [SerpAPI](https://serpapi.com/) (for using the SerpAPIWrapper tool).
- Basic knowledge of Python programming and Streamlit.

## Getting Started

### Installation

1. Clone the Langchain Agents repository to your local machine:

   ```bash
   git clone https://github.com/your-username/langchain-agents.git
   ```

2. Change the directory to the project folder:

   ```bash
   cd langchain-agents
   ```

3. Install the required Python packages using pip:

   ```bash
   pip install -r requirements.txt
   ```

### Configuration

To configure the application, you need to set up your API keys for OpenAI and SerpAPI. Follow these steps:

1. Obtain an API key for OpenAI by signing up at [OpenAI](https://beta.openai.com/signup/).

2. Obtain an API key for SerpAPI by signing up at [SerpAPI](https://serpapi.com/).

3. Open the `app.py` file and replace the following lines with your API keys:

   ```python
   OPENAI_API_KEY = "your_openai_api_key_here"
   SERPAPI_API_KEY = "your_serpapi_api_key_here"
   ```

   Replace `"your_openai_api_key_here"` and `"your_serpapi_api_key_here"` with your actual API keys.

## Usage

### Running the Application

To run the Langchain Agents application, execute the following command in your terminal:

```bash
streamlit run app.py
```

This will start the Streamlit development server, and the application will be accessible in your web browser at `http://localhost:8501`.

### Simulating Conversations

1. Once the application is running, you'll see a chat interface.

2. Enter your messages in the chat input labeled "You (Incident Manager): Enter your message."

3. The application will simulate responses from three virtual agents: Ben (CEO), Tyne (CTO), and DA (Assistant).

4. Agent responses will be displayed in the chat history with their respective roles.

## Customizing Agents

You can customize the agent templates and responses by modifying the code in the `app.py` file. Each agent's template is defined using a prefix and a suffix. You can adjust the text and role descriptions as needed.

```python
ben_suffix = """Your name is Ben you are the (CEO)
# ... (Agent's description and template)
"""

# Create agents with custom templates
ben_agent = create_agent("Ben", prefix, ben_suffix)
```

Feel free to modify the templates and agent roles to fit your application's requirements.

## Contributing

Contributions to this project are welcome. You can contribute by:

- Reporting issues or suggesting enhancements.
- Making code contributions through pull requests.
- Improving documentation and README.

Please read the [Contribution Guidelines](CONTRIBUTING.md) for more details on how to contribute.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
