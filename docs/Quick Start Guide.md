# 🤖 AI Prompt Engineer - Quickstart Guide 🚀


## Table of Contents 📑
- [1. Introduction](#1-introduction)
- [2. Setup and Installation](#2-setup-and-installation)
    - [2.1 Installing Cursor Editor](#21-installing-cursor-editor)
    - [2.2 Installing Miniconda](#22-installing-miniconda)
        - [2.2.1 Windows Installation](#221-windows-installation)
        - [2.2.2 MacOS Installation](#222-macos-installation)
    - [2.3 Creating a Conda Environment](#23-creating-a-conda-environment)
    - [2.4 Getting Your API Keys](#24-getting-your-api-keys)
        - [2.4.1 Langsmith API Key](#241-langsmith-api-key)
        - [2.4.2 Groq API Key](#242-groq-api-key)
- [3. User Interface Overview](#3-user-interface-overview)
- [4. Features ✨](#4-features)
    - [4.1 Generate Prompt ✍️](#41-generate-prompt)
    - [4.2 Generate Dataset 📊](#42-generate-dataset)
    - [4.3 Help Section ❓](#43-help-section)
- [5. Settings and Configuration ⚙️](#5-settings-and-configuration)
- [6. Advanced Features 🚀](#6-advanced-features)
    - [6.1 Chain of Thought (COT) Prompting 🧠](#61-chain-of-thought-cot-prompting)
    - [6.2 Langsmith Tracing and Observability 🕵️‍♀️](#62-langsmith-tracing-and-observability)
    - [6.3 Dynamic Model Selection 🔄](#63-dynamic-model-selection)
    - [6.4 Adaptive Temperature and Token Management 🌡️](#64-adaptive-temperature-and-token-management)
    - [6.5 Test Data Generation for AI Fine-Tuning 🧪](#65-test-data-generation-for-ai-fine-tuning)
- [7. Troubleshooting 🧰](#7-troubleshooting)
- [8. Best Practices 👍](#8-best-practices)
- [9. FAQ 🤔](#9-faq)
- [10. Version History 🕰️](#10-version-history)


  ![App Tree Flow Quick Start](https://github.com/user-attachments/assets/774587c8-88e1-431a-9e34-d8f2fd507b52)




## 1. Introduction <a name="1-introduction"></a>


The AI Prompt Engineer is a powerful Streamlit application designed to assist users in generating effective prompts for AI models and creating datasets for AI fine-tuning. It leverages Groq's Llama 3 AI models to provide advanced language processing capabilities. 🧠


Key Features:
- Generate AI/LLM prompts using Chain of Thought (COT) methodology 🧠
- Generate test datasets for AI model fine-tuning 📊
- Customizable settings for AI model parameters ⚙️


  ![COT features-selection](https://github.com/user-attachments/assets/408a627f-ad35-49fc-bded-000df5d0cc22)




## 2. Setup and Installation <a name="2-setup-and-installation"></a>


To run the AI Prompt Engineer application, you'll need to set up your environment and install the necessary dependencies. 🏗️


### 2.1 Downloading and Installing Cursor Editor <a name="21-installing-cursor-editor"></a>


1. **Visit Cursor's website:** https://www.cursor.com/
2. **Download Cursor:** Choose the version suitable for your operating system (Windows, macOS, Linux).
3. **Install Cursor:** Run the downloaded installer and follow the prompts.
4. **Open Cursor:** Once installed, open the application.

![Download the Cursor AI Code Editor](https://github.com/user-attachments/assets/7101362c-79e7-4206-bdf9-4c8b7657c709)

### 2.2 Installing Miniconda <a name="22-installing-miniconda"></a>


Miniconda is a minimal installer for Conda, which we'll use to manage our Python environments. 🐍


#### 2.2.1 Windows Installation <a name="221-windows-installation"></a>


1. Visit the Miniconda download page: https://docs.conda.io/en/latest/miniconda.html
2. Download the appropriate installer for your Windows system architecture (32-bit or 64-bit).
3. Run the downloaded installer.
4. Follow the installation wizard, using the default options unless you have specific preferences.
5. **Important:** During installation, make sure to check the box that says "Add Miniconda3 to my PATH environment variable".
6. After installation, open a new Command Prompt and verify by running:


```bash
conda --version
```


#### 2.2.2 MacOS Installation <a name="222-macos-installation"></a>


1. Visit the Miniconda download page: https://docs.conda.io/en/latest/miniconda.html
2. Download the MacOS installer PKG (choose the appropriate version for your system architecture).
3. Navigate to the folder where you downloaded the file.
4. Double click to install the version for Intel or M1,M2,M3 Metal pkg:




```
Intel: https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.pkg
Metal: https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64


```


5. Follow the prompts to complete the installation:


```
Close and reopen the Cursor Terminal to apply the changes.
```


### 2.3 Creating a Conda Environment <a name="23-creating-a-conda-environment"></a>


1. Open your terminal (Command Prompt for Windows, Terminal for macOS).
2. Create a new Conda environment named `streamlit-env` with Python 3.12 (or your preferred version):


![Installing conda](https://github.com/user-attachments/assets/67f134ca-e026-4864-9506-d070431457c8)


```bash
conda create --name streamlit-env python=3.12
```


3. Activate the new environment:


```bash
conda activate streamlit-env
```


4.  **To deactivate the environment later:**


```bash
conda deactivate
```


### 2.4 Getting Your API Keys <a name="24-getting-your-api-keys"></a>


#### 2.4.1 Langsmith API Key <a name="241-langsmith-api-key"></a>


LangSmith is a tool for observing, debugging, dataset creation, cost analysis, and improving your AI/LLM applications. 


![Langsmith Usage Funnel](https://github.com/user-attachments/assets/beace749-eb78-4a1f-bd68-b1d125504c88)


1. Get your Langsmith API Key here: https://smith.langchain.com/
2. Sign up for a free account or log in if you already have one.
3. You'll find your API key in your account settings.


#### 2.4.2 Groq API Key <a name="242-groq-api-key"></a>


Groq API Key: This special key allows you to tap into Groq's powerful AI models. 


1. Get your free key at: https://groq.com/developers.
2. Sign up for a free account or log in if you already have one.
3. You'll find your API key in your account settings.


**How to use the Groq API Key:** Enter this special key in the left side of the Streamlit frontend UI in order to use the app.


### Prerequisites:
- Python 3.11 or higher 🐍
- pip (Python package manager) 📦


### Installation Steps:


1. Clone the repository or download the source code. 📥


2. Install required packages:
   ```
   pip install streamlit groq python-dotenv langsmith pandas PyPDF2 streamlit-extras streamlit-option-menu streamlit-lottie requests
   ```


3. Set up environment variables:
   Create a `.env` file in the project root directory and add the following:
   ```
   LANGCHAIN_TRACING_V2=true
   LANGCHAIN_ENDPOINT=https://api.smith.langchain.com
   LANGCHAIN_API_KEY=your_langchain_api_key
   GROQ_API_KEY=your_groq_api_key
   ```


4. Run the application:
   ```
   streamlit run v1.95-groq-prompt-engineer.py
   ```


## 3. User Interface Overview <a name="3-user-interface-overview"></a>


The application features a clean and intuitive user interface divided into several sections:


- Header: Displays the application title and logo 📝
- Navigation Menu: Horizontal menu for switching between main features 🧭
- Main Content Area: Changes based on the selected feature 🖼️
- Sidebar: Contains settings and configuration options ⚙️


The navigation menu includes the following options:
- Generate Prompt ✍️
- Generate Dataset 📊
- Help ❓


## 4. Features <a name="4-features"></a>


### 4.1 Generate Prompt <a name="41-generate-prompt"></a>


This feature allows users to create AI-generated prompts based on their input. ✍️


How to use:
1. Enter your question or task in the text area. 📝
2. Optionally, provide input variables (comma-separated). 🗃️
3. Click the "Generate Prompt" button. ➡️
4. View the generated prompt and download options. 👀


Example input variables:
- topic, audience, tone
- product_name, target_market, unique_selling_point
- character_name, setting, genre


### 4.2 Generate Dataset <a name="42-generate-dataset"></a>


This feature helps users create test datasets for AI model fine-tuning. 📊


How to use:
1. Enter a topic or text for test data generation. 📝
2. Specify the number of conversation pairs to generate (1-100). 🔢
3. Click the "Generate Test Data" button. ➡️
4. View the generated conversation pairs. 👀
5. Download the data as JSON or JSONL format. 📥


### 4.3 Help Section <a name="43-help-section"></a>


The Help section provides detailed information on how to use the application, including:
- Step-by-step instructions for each feature 👣
- Tips for achieving better results 💡
- FAQ addressing common questions and concerns ❓


## 5. Settings and Configuration <a name="5-settings-and-configuration"></a>


The sidebar contains important settings and configuration options:


- API Key Input: Enter your Groq API key (required for functionality) 🔑
- Model Selection: Choose between different Groq Llama 3 model versions 🤖
- Temperature Slider: Adjust the creativity/randomness of the AI output (0.0 to 1.5) 🌡️
- Max Output Tokens: Set the maximum length of the AI-generated content (1024 to 8192) 💬


## 6. Advanced Features <a name="6-advanced-features"></a>


### 6.1 Chain of Thought (COT) Prompting <a name="61-chain-of-thought-cot-prompting"></a>


The  application utilizes Chain of Thought (COT) prompting to generate more effective and detailed AI responses. This approach breaks down complex tasks into logical steps, encouraging the AI model to show its reasoning process. 🧠


![COT Steps](https://github.com/user-attachments/assets/e94ce1bc-8ea1-4acf-9797-8bf88f5376bd)


Key aspects of COT prompting in :
- Task analysis and breakdown 🔍
- Incorporation of provided variables 🗃️
- Adaptation to specific Groq model capabilities 🤖
- Optimization for clarity and specificity 🎯
- Inclusion of context and formatting instructions 📝
- Encouragement of creativity and problem-solving 💡
- Consideration of error handling and edge cases ⚠️


### 6.2 Langsmith Tracing and Observability <a name="62-langsmith-tracing-and-observability"></a>


The application integrates Langsmith for tracing and observability of AI interactions. This feature helps in monitoring and analyzing the performance of the AI prompts and responses. 🕵️‍♀️


To enable Langsmith tracing:
1. Ensure the `LANGCHAIN_TRACING_V2` environment variable is set to `true`. 
2. Provide your Langsmith API key in the `.env` file. 


Benefits of Langsmith integration:
- Track and analyze AI prompt effectiveness 📈
- Identify patterns in user queries and AI responses 🔎
- Optimize application performance and resource usage ⏱️


### 6.3 Dynamic Model Selection <a name="63-dynamic-model-selection"></a>


Users can select different versions of the Groq Llama 3 model based on their specific needs:


- llama3-70b-8192: Large model with high performance 🏋️‍♀️
- llama3-8b-8192: Smaller model with faster inference 🏃‍♀️
- llama3-groq-70b-8192-tool-use-preview: Specialized for tool use 🧰
- llama3-groq-8b-8192-tool-use-preview: Smaller tool-use model 🧰
- llama-3.1-8b-instant: Fast and efficient model ⚡️
- llama-3.1-70b-versatile: Versatile model for various tasks 🦸‍♀️


![Groq Llama3 Model Overview](https://github.com/user-attachments/assets/6a5f65c9-6e14-445d-bb28-a971f97bb440)




The application dynamically adjusts its prompting strategy based on the selected model to leverage each version's strengths.


### 6.4 Adaptive Temperature and Token Management <a name="64-adaptive-temperature-and-token-management"></a>


The temperature and max output tokens settings allow for fine-tuned control over the AI's output:


- Temperature (0.0 to 1.5):
  - Lower values: More focused and deterministic responses 🎯
  - Higher values: More creative and diverse outputs 💡


- Max Output Tokens (1024 to 8192):
  - Adjust based on the complexity of the task and desired response length 💬
  - Helps in managing API usage and response time ⏱️


### 6.5 Test Data Generation for AI Fine-Tuning <a name="65-test-data-generation-for-ai-fine-tuning"></a>


The test data generation feature creates structured datasets suitable for fine-tuning language models:


- Generates pairs of human messages and AI responses 💬
- Outputs data in both JSON and JSONL formats 📥
- Allows customization of topic and number of conversation pairs 📝


Use cases for generated test data:
- Fine-tuning custom AI models 🤖
- Evaluating AI performance on specific topics 📈
- Creating benchmarks for AI system testing 🧪


## 7. Troubleshooting <a name="7-troubleshooting"></a>


### 7.1 API Key Issues


If you encounter problems related to the Groq API key:
1. Ensure the API key is entered correctly in the sidebar. 🔑
2. Check that your API key has the necessary permissions and quota. 🔒
3. Verify your internet connection to ensure the API can be reached. 🌐


### 7.2 Model Performance Issues


If the AI-generated content is not meeting expectations:
1. Try adjusting the temperature setting to find the right balance of creativity and focus. 🌡️
2. Increase the max output tokens if responses seem truncated. 
3. Experiment with different model versions to find the best fit for your use case. 🤖


### 7.3 Test Data Generation Errors


If test data generation is not working as expected:
1. Verify that the topic input is clear and specific. 
2. Try generating a smaller number of conversation pairs first. 
3. Check the console logs for any error messages related to JSON parsing. 


## 8. Best Practices <a name="8-best-practices"></a>


To get the most out of the AI Prompt Engineer application, consider the following best practices:


### 8.1 Prompt Generation
- Be specific and clear in your task description. 🎯
- Provide relevant context and constraints. 
- Use input variables effectively to create more dynamic prompts. 
- Iterate on prompts based on the AI's output to refine results. 


### 8.2 Test Data Generation
- Choose diverse and representative topics for your dataset. 
- Generate larger datasets for more comprehensive fine-tuning. 
- Review and potentially curate the generated data before use. 


### 8.3 Model and Settings Selection
- Experiment with different model versions for various tasks. 🤖
- Adjust temperature based on whether you need more deterministic or creative outputs. 🌡️
- Balance max output tokens with your task complexity and API usage considerations. 💬


## 9. FAQ <a name="9-faq"></a>


### Q1: What is the difference between the Groq Llama 3 model versions?
A1: The Groq Llama 3 model versions offer different balances of speed, capability, and features. The smaller models (e.g., llama3-8b-8192) are faster but may have lower accuracy than the larger models (e.g., llama3-70b-8192). Some models are specialized for specific tasks, like tool use. Refer to the Groq documentation for detailed comparisons.


### Q2: How do I choose the right temperature setting?
A2: The temperature setting (0.0 to 1.5) affects the creativity and randomness of the AI's output. Lower values (closer to 0) produce more focused and deterministic responses, while higher values (closer to 1.5) generate more diverse and creative outputs. Experiment with different values to find the right balance for your specific use case.


### Q3: How can I use the generated test data for AI fine-tuning?
A3: The test data generated by the application can be used to fine-tune AI models by providing examples of human-AI interactions. You can download the data in JSON or JSONL format and use it with AI training frameworks or APIs that support fine-tuning.


### Q4: Is my data secure when using this application?
A4: The application processes data locally and only sends prompts and content to the Groq API for processing. However, users should be cautious about uploading sensitive information and refer to Groq's data privacy policies regarding the use of the Groq API.


### Q5: Can I use the application offline?
A5: The core functionality of the application requires an internet connection to communicate with the Groq API. However, some features like file viewing may work offline.


### Q6: How can I improve the quality of generated prompts?
A6: To improve prompt quality, provide clear and specific task descriptions, include relevant context, use input variables effectively, and iterate on your prompts based on the AI's responses.


## 10. Version History <a name="10-version-history"></a> 


### v1.9.5 (Current Version)
- Refactored to use Groq API and Models
- Added support for streaming output from the Groq API
- Updated UI to reflect the use of Groq
- Updated User Guide and FAQ to provide information about Groq
- Removed Analyze File Feature


### v1.9 
- Enhanced file analysis capabilities
- Improved dataset generation feature
- Updated user interface with new animations
- Added support for PDF file analysis
- Implemented Langsmith tracing for better observability
- Expanded temperature range to 1.5


## 11. Possible Future Development Roadmap


While not currently implemented, the following features are ideas for future versions:


### 11.1 Multi-Language Support
- Ability to generate prompts and analyze content in multiple languages 🌎
- Language detection and translation features 🗣️


### 11.2 Advanced Visualization
- Integration of data visualization tools for better insight into analyzed files 📊
- Interactive charts and graphs for test data generation results 📈


### 11.3 Collaborative Features
- User accounts and saved prompts/analyses 👤
- Ability to share and collaborate on prompt engineering projects 🤝


### 11.4 API Integration
- Option to integrate with other AI APIs for comparison and enhanced capabilities 🤖
- Custom API endpoint configuration for enterprise users 🏢


### 11.5 Prompt Templates and Libraries
- Pre-built prompt templates for common use cases 📝
- User-contributed prompt library with rating and commenting features 👍👎


## 12. Community and Support


### 12.1 Contributing to AI Prompt Engineer
The AI Prompt Engineer is an open-source project, and contributions from the community are welcome. To contribute:
1. Fork the repository on GitHub 🍴
2. Create a new branch for your feature or bug fix 
3. Submit a pull request with a clear description of your changes 


### 12.2 Reporting Issues
If you encounter bugs or have feature requests:
1. Check the existing issues on the GitHub repository 
2. If your issue isn't already reported, create a new issue with a detailed description 


### 12.3 Community Resources
- Join the AI Prompt Engineer user forum (link to be provided) 💬
- Follow the project on social media for updates and tips 📣
- Attend virtual meetups and webinars on prompt engineering (schedule to be announced) 


## 13. Glossary of Terms


- **Chain of Thought (COT)**: A prompting technique that breaks down complex tasks into steps, encouraging the AI to show its reasoning process. 🧠
- **Temperature**: A setting that controls the randomness and creativity of the AI's output. 🌡️
- **Max Output Tokens**: The maximum number of tokens (words or word pieces) the AI model will generate in its response. 💬
- **Fine-Tuning**: The process of further training an AI model on a specific dataset to improve its performance on particular tasks or domains. ⚙️
- **Prompt Engineering**: The practice of designing and optimizing input prompts to elicit desired responses from AI language models. ✍️
- **Groq API**: Groq's API for accessing the Groq series of AI models. 💻
- **Langsmith**: A tool for tracing and observing AI model interactions and performance. 🕵️‍♀️


## Conclusion


The AI Prompt Engineer (APE) application is a powerful tool for anyone working with AI language models, from beginners to advanced users. By leveraging the capabilities of Groq's Llama 3 models and providing an intuitive interface for prompt generation and dataset creation, APE streamlines the process of prompt engineering and AI interaction.


As the field of AI continues to evolve rapidly, tools like APE play a crucial role in helping users harness the full potential of large language models. Whether you're developing AI applications, conducting research, or simply exploring the capabilities of AI, APE provides the features and flexibility to support your needs.


We encourage users to explore all aspects of the application, experiment with different settings and approaches, and contribute to the ongoing development of this open-source tool. Your feedback and contributions are invaluable in shaping the future of AI prompt engineering and making these powerful technologies more accessible to a wider audience.


Thank you for using AI Prompt Engineer. We look forward to seeing the innovative ways you'll use this tool to push the boundaries of what's possible with AI language models.
--- END OF FILE # 🤖 AI Prompt Engineer - Quickstart Guide 🚀.txt ---
