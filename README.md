# YTChatFlow-AI-Assistant-for-YouTube-via-LangChain
YTChatFlow is an AI-powered YouTube assistant that extracts transcripts, creates embeddings, and uses LangChain RAG to provide summaries, Q&amp;A, and insights from videos. It helps users quickly understand long content through an interactive chat-based experience.


This project is an AI-powered chatbot that answers questions about any YouTube video using its transcript. It utilizes:
- 🧠 Google Gemini (Generative AI)
- 🧾 YouTube Transcript API
- 🔍 LangChain for vector search
- 🗃️ FAISS for persistent storage


## 🚀 Features

- 🔎 Automatically fetches transcript of a given YouTube video
- 🌐 Translates non-English transcripts to English (if needed)
- 🧱 Splits and embeds the transcript using GoogleEmbeddings
- 🧠 Uses Gemini AI to answer questions based on transcript context
- 💾 Stores vector data with Chroma for retrieval

## 🧰 Tech Stack

| Layer         | Technology              |
|--------------|--------------------------|
| Backend       | Python, FastAPI         |
| LLM & Embeddings | Google Gemini + LangChain |
| Transcript    | YouTube Transcript API |
| Vector DB     | FAISS (Persistent)     |


## 💬 How It Works

1. User enters a **YouTube video ID** and a **question** in the chatbot UI.
2. The **backend fetches the transcript** using `youtube_transcript_api`.
3. If the transcript is in a non-English language, it uses **Gemini** to translate it to English.
4. The transcript is **split into chunks** using LangChain's `RecursiveCharacterTextSplitter`.
5. These chunks are **embedded using Gemini embeddings**.
6. Embeddings are stored in **FAISS** for efficient similarity search.
7. The user's query is **matched against similar chunks** from the transcript.
8. **Gemini** is prompted with the most relevant transcript chunks and **returns an answer**.

---

## 🧪 Example Query

- **Video ID:** `k8Y6SQYfQ4s`  
- **Question:** "Is there discussion about Ajay Devgan in the video?"  
- **Answer:** "Yes, Ajay Devgan was mentioned in the context of..."
