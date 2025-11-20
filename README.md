🌐 AI-Powered Hindi & Telugu Translation System

A lightweight and efficient English-to-Hindi and English-to-Telugu translation application built with Streamlit, n8n, and Gemini AI.
This project demonstrates how workflow automation and LLM intelligence can deliver fast, accurate, and real-time translation.

🚀 Features

🔤 Translate English → Hindi or Telugu

⚡ Real-time output using Streamlit UI

🔗 Webhook-based automation through n8n

🧠 AI-powered translation using Gemini AI

🧩 Clean integration of frontend and backend

🛠️ Easily customizable prompts and logic

🏗️ Project Architecture
Streamlit Frontend  →  n8n Webhook  →  AI Agent Node (Gemini) → Response to Streamlit

🖼️ Workflow Overview (n8n)

Webhook Node
Receives text input from the Streamlit app.

AI Agent Node (Gemini)
Uses a custom system prompt to translate text into either Hindi or Telugu.

Respond to Webhook
Sends translated text back to the Streamlit app.
