# 🤖 Agentic AI Learning Journey

[![Learning Progress](https://img.shields.io/badge/Day-2-blue.svg)](https://github.com/yourusername/agentic-ai-day2)
[![Status](https://img.shields.io/badge/Status-Implementation-green.svg)](https://github.com/yourusername/agentic-ai-day2)
[![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange.svg)](https://colab.research.google.com/)

## 📚 Overview

Day 2 marks the transition from concepts to code! This repository contains my first hands-on implementation of integrating a Large Language Model (LLM) using Groq API and LangChain.

**What I Built:** A basic LLM integration using Groq's Llama 3.3 model through LangChain in Google Colab.

---

## 🎯 Learning Objectives

- ✅ Set up API keys securely in Google Colab
- ✅ Install and import LangChain with Groq
- ✅ Initialize an LLM client
- ✅ Make my first LLM API call using the `invoke` method

---

## 🛠️ Technologies Used

- **Platform:** Google Colab
- **API Provider:** Groq
- **Framework:** LangChain
- **Model:** Llama 3.3 70B Versatile
- **Language:** Python

---

## 📋 Step-by-Step Implementation - Google Colab

### Step 1: Secure API Key Setup
Store your Groq API key in Google Colab's secret key section.

**How to add secrets in Colab:**
1. Click the 🔑 key icon in the left sidebar
2. Add a new secret
3. Name it (e.g., `API_1`)
4. Paste your Groq API key

### Step 2: Install Required Libraries
```python
!pip install langchain_groq
```

### Step 3: Import Necessary Libraries
```python
from google.colab import userdata
from langchain_groq import ChatGroq
```

### Step 4: Retrieve API Key
```python
# Call the API key from Google Colab secrets
groq_api = userdata.get('API_1')
```

### Step 5: Initialize the LLM
```python
# Pass required parameters: api_key and model_name
llm = ChatGroq(
    api_key=groq_api,
    model='llama-3.3-70b-versatile'
)
```

### Step 6: Invoke the Model
```python
# Ask your first question
response = llm.invoke('What is Notepad?')
print(response)
```

---

## 🔑 Key Concepts Learned

### 1. **Secure API Key Management**
- Never hardcode API keys in your code
- Use Google Colab's `userdata` for secure storage
- Access keys only when needed

### 2. **LangChain Abstraction**
- LangChain provides a unified interface for different LLM providers
- Easy to switch between providers (OpenAI, Groq, Anthropic, etc.)
- Consistent API across models

### 3. **Model Invocation**
- `invoke()` method sends a single query to the LLM
- Returns a response object
- Synchronous operation (waits for response)

---

## 📊 Expected Output

```
What is Notepad?

Notepad is a simple text editor that comes pre-installed with Microsoft Windows. 
It's designed for creating and editing plain text files with a .txt extension. 
Notepad is lightweight, fast, and provides basic text editing functionality without 
complex formatting options...
```

---

## 🚀 How to Run This Code

### Prerequisites
- Google Account (for Colab access)
- Groq API Key ([Get one here](https://console.groq.com/))

### Steps
1. Open [Google Colab](https://colab.research.google.com/)
2. Create a new notebook
3. Add your Groq API key to Colab secrets (name it `API_1`)
4. Copy and paste the complete code
5. Run all cells
6. See the magic happen! ✨

## 🐛 Common Issues & Solutions

### Issue 1: API Key Not Found
```
Error: Secret 'API_1' not found
```
**Solution:** Make sure you've added the API key in Colab's secrets section with the exact name `API_1`.

### Issue 2: Module Not Found
```
ModuleNotFoundError: No module named 'langchain_groq'
```
**Solution:** Run `!pip install langchain_groq` before importing.

### Issue 3: Invalid API Key
```
Error: Invalid API key
```
**Solution:** Verify your API key is correct and active on [Groq Console](https://console.groq.com/).

## 🎓 Key Takeaways

- ✅ Successfully integrated Groq API with LangChain
- ✅ Learned secure API key management in Colab
- ✅ Made my first LLM API call
- ✅ Understanding the basic structure of LLM invocation
- ✅ Foundation for building more complex AI systems

---
###  ⬅️ Previous
 [Day 1: Core Concepts](https://github.com/lookmohan/Agentic-AI)

###  ➡️ Next
 [Day 3: Prompt Technique]githublinkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkk

---

## 🤝 Connect & Learn Together

If you're also learning about Agentic AI, feel free to:
- ⭐ Star this repository
- 🔄 Fork and experiment with the code
- 💬 Open an issue to discuss implementations
- 📧 Reach out: [mohanraj9677011@gmail.com]

---

## 📖 Additional Resources

- [Groq Documentation](https://console.groq.com/docs)
- [LangChain Documentation](https://python.langchain.com/)
- [Google Colab Guide](https://colab.research.google.com/)
- [Llama 3.3 Model Card](https://www.llama.com/)

---

## 📝 License

This learning repository is open-source and available under the [MIT License](LICENSE).
