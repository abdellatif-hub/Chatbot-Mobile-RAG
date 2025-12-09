# 🚀 RAG Multimodal : OpenAI + PostgreSQL + pgvector + Streamlit + FastAPI

Un système **RAG (Retrieval-Augmented Generation)** capable d’analyser des **PDF**, d’indexer automatiquement leur contenu (texte + captions d’images), puis de répondre intelligemment aux questions de l’utilisateur.

Ce projet combine :
- 🧠 **OpenAI GPT-5**  
- 📄 **pypdf** pour extraire le texte  
- 🖼️ **OpenAI Vision** pour générer des captions  
- 🗃️ **PostgreSQL + pgvector** pour stocker les embeddings  
- 🌐 **FastAPI** comme API backend  
- 🖥️ **Streamlit** comme interface graphique  
- 🔍 **RAG Pipeline complet**

---
<img width="2000" height="1126" alt="Advanced-RAG" src="https://github.com/user-attachments/assets/10ffd697-25e7-4f99-9422-e1bc87a10731" />

---
## 📁 Structure du projet
````
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
````

<img width="730" height="827" alt="Capture d&#39;écran 2025-12-02 205053" src="https://github.com/user-attachments/assets/b05c76a7-a97e-441a-838f-a62ef14c6309" />


---
# 2️⃣ Lancer PostgreSQL + pgvector
````
docker-compose up -d
````

<img width="1859" height="157" alt="image" src="https://github.com/user-attachments/assets/55004808-f5f0-43af-bdf7-da5b59127509" />

---
# 3️⃣ Créer et activer le virtualenv
````
python -m venv venv
venv\Scripts\activate.bat
````
<img width="1866" height="81" alt="image" src="https://github.com/user-attachments/assets/43934159-d006-4c6e-99a2-674c8245397e" />

<img width="1861" height="89" alt="image" src="https://github.com/user-attachments/assets/73a44f4a-0ef9-4af8-8b01-70ab755a02ef" />

---
# 4️⃣ Installer les dépendances
````
pip install -r requirements.txt
````

<img width="1864" height="1104" alt="image" src="https://github.com/user-attachments/assets/a7368bb9-fa89-4b37-9921-ad692e811c92" />

---
# 📥 Ingestion des PDF et images

## Ajoute tes fichiers dans :

````
data/
````
<img width="2557" height="1079" alt="image" src="https://github.com/user-attachments/assets/0943f6b6-6a6d-4f18-acc0-0a5327d3499d" />

## Puis lance :
````
python ingest.py
````

## ✔ Résultat attendu

<img width="1871" height="187" alt="image" src="https://github.com/user-attachments/assets/c4bb7df1-904f-4b90-8b6e-19177b078d69" />

---
# 🧠 Interface Web (Streamlit)

## Pour lancer l’UI :
````
streamlit run app.py
````

<img width="1863" height="583" alt="image" src="https://github.com/user-attachments/assets/be96a8cb-c6fc-4833-9ab9-48a4e127397f" />
<img width="2559" height="1275" alt="image" src="https://github.com/user-attachments/assets/2507731b-45dc-4ed9-8bea-ead9e8f62210" />

---
# 🌐 API REST (FastAPI)

## ✅ 1. Crée un fichier api.py
<img width="2559" height="1146" alt="image" src="https://github.com/user-attachments/assets/7aadf4d8-c020-4587-9226-435e46ab8ed6" />

---
## ✅ 2. Installer FastAPI + Uvicorn 
````
pip install fastapi uvicorn
````
<img width="1863" height="1167" alt="image" src="https://github.com/user-attachments/assets/bf6607db-bc21-4b40-9ebc-a9737fb5b078" />

## ✅ 3. Lancer l’API
````
uvicorn api:app --reload
````
<img width="1847" height="1074" alt="image" src="https://github.com/user-attachments/assets/713f570b-f6c0-4fce-b16c-142d0a487542" />

---
## ✅ 4. Tester dans le navigateur ou Postman
````
Méthode : GET
````
<img width="1802" height="1205" alt="image" src="https://github.com/user-attachments/assets/66b1f138-709f-4525-aea3-50b5e3c3abf3" />

---

````
Méthode : POST
````
<img width="2559" height="1345" alt="image" src="https://github.com/user-attachments/assets/46c53840-93fd-4112-b40e-37702d97a3da" />






