# 🚀 RAG Multimodal : OpenAI + PostgreSQL + pgvector + Streamlit + FastAPI

Un système **RAG (Retrieval-Augmented Generation)** capable d’analyser des **PDF + Images**, d’indexer automatiquement leur contenu (texte + captions d’images), puis de répondre intelligemment aux questions de l’utilisateur.

Ce projet combine :
- 🧠 **OpenAI GPT-5**  
- 📄 **pypdf** pour extraire le texte  
- 🖼️ **OpenAI Vision** pour générer des captions  
- 🗃️ **PostgreSQL + pgvector** pour stocker les embeddings  
- 🌐 **FastAPI** comme API backend  
- 🖥️ **Streamlit** comme interface graphique  
- 🔍 **RAG Pipeline complet**

---

## 📁 Structure du projet

rag_multi_modal/
│── api.py # API FastAPI pour requêtes GET
│── app.py # Application Streamlit
│── db.py # Connexion PostgreSQL
│── db.sql # Création de la table pgvector
│── docker-compose.yml # PostgreSQL + pgvector
│── ingest.py # Pipeline ingestion PDF + images
│── openai_utils.py # Caption + Embedding
│── rag_core.py # Retrieval + génération RAG
│── requirements.txt # Dépendances
│── data/ # Dossier PDF/Images à indexer
│── venv/ # Environnement virtuel
<img width="696" height="1284" alt="image" src="https://github.com/user-attachments/assets/e9d86de2-c847-4cf5-abbf-cc3ebbaba24a" />
2️⃣ Lancer PostgreSQL + pgvector
docker-compose up -d


