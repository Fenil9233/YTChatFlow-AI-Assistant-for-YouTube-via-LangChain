# YTChatFlow-AI-Assistant-for-YouTube-via-LangChain
YTChatFlow is an AI-powered YouTube assistant that extracts transcripts, creates embeddings, and uses LangChain RAG to provide summaries, Q&amp;A, and insights from videos. It helps users quickly understand long content through an interactive chat-based experience.


This project is an AI-powered chatbot that answers questions about any YouTube video using its transcript. It utilizes:

🧠 Google Gemini (Generative AI)
🧾 YouTube Transcript API
🔍 LangChain for vector search
🗃️ FAISS for persistent storage
🌐 FastAPI for the backend server

🚀 Features
🔎 Automatically fetches transcript of a given YouTube video
🌐 Translates non-English transcripts to English (if needed)
🧱 Splits and embeds the transcript using GoogleEmbeddings
🧠 Uses Gemini AI to answer questions based on transcript context
💾 Stores vector data with Chroma for retrieval
