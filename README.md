# 🌐 **AI-Powered Hindi & Telugu Translation System**

A lightweight and efficient **English-to-Hindi** and **English-to-Telugu** translation application built with **Streamlit**, **n8n**, and **Gemini AI**.
This project demonstrates how workflow automation and LLM intelligence can deliver fast, accurate, and real-time translation.

---

## 🚀 **Features**

* 🔤 **Translate English → Hindi or Telugu**
* ⚡ **Real-time output** using Streamlit UI
* 🔗 **Webhook-based automation** through n8n
* 🧠 **AI-powered translation** using Gemini AI
* 🧩 **Clean integration** of frontend and backend
* 🛠️ **Easily customizable** prompts and logic

---

## 🏗️ **Project Architecture**

```
Streamlit Frontend  →  n8n Webhook  →  AI Agent Node (Gemini) → Response to Streamlit
```

---

## 🖼️ **Snapshot**


<img width="1913" height="928" alt="AI Translator" src="https://github.com/user-attachments/assets/db8a63bd-73a6-462c-9dfc-802c8f191a07" />


---

## 🖥️ **Workflow Overview (n8n)**

1. **Webhook Node** – Receives text input
2. **AI Agent Node (Gemini)** – Performs Hindi / Telugu translation
3. **Respond to Webhook Node** – Sends output back

---

## 🧩 **System Prompts Used**

### **Hindi Translation Prompt**

```
You are a professional translator.
Translate the given English text into pure Hindi.
Output should contain only the translated Hindi sentence.
Do not add explanations.
```

### **Telugu Translation Prompt**

```
You are a professional translator.
Translate the given English text into pure Telugu.
Output should contain only the translated Telugu sentence.
Do not add explanations.
```

---

## 🖥️ **Streamlit Code (Example)**

```python
import streamlit as st
import requests

st.title("Instant AI Translator")
st.subheader("Translate English text into Hindi or Telugu instantly")

text = st.text_area("Enter English Text")

TELUGU_WEBHOOK = "YOUR_TELUGU_WEBHOOK_URL"
HINDI_WEBHOOK = "YOUR_HINDI_WEBHOOK_URL"

if st.button("Translate to Telugu"):
    if text:
        response = requests.post(TELUGU_WEBHOOK, json={"text": text})
        st.write(response.text)

if st.button("Translate to Hindi"):
    if text:
        response = requests.post(HINDI_WEBHOOK, json={"text": text})
        st.write(response.text)
```

---

## 📦 **Requirements**

```
pip install streamlit requests
```

---

## ▶️ **Run the App**

```
streamlit run app.py
```
