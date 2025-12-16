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


--- 

# 🤖 RAG Multimodal Chatbot Frontend
### Flutter • FastAPI • PostgreSQL (pgvector) • OpenAI

> 📌 **Projet académique – Chatbot RAG Multimodal**  
> Ce projet implémente un **chatbot intelligent** capable de répondre à des questions **à partir de documents PDF (PFE)** en utilisant une architecture **RAG (Retrieval-Augmented Generation)**.

---

## 🧠 Objectif du projet

L’objectif est de concevoir une application mobile Flutter qui permet à un utilisateur de poser des questions, et d’obtenir des réponses **basées uniquement sur le contenu d’un document PDF** grâce à :

- la **recherche vectorielle (pgvector)**
- les **embeddings OpenAI**
- un **backend FastAPI**
- une **interface mobile Flutter**

---

## 🏗️ Architecture globale

```
Flutter (Mobile App)
│
│ HTTP POST /rag-chat
▼
FastAPI (Backend RAG)
│
│ Similarity Search (pgvector)
▼
PostgreSQL + pgvector
│
▼
OpenAI (Embeddings + LLM)

```

--- 

## 🧰 Technologies utilisées

### 🔹 Frontend
- Flutter
- Dart
- Dio & Retrofit

### 🔹 Backend
- Python
- FastAPI
- Uvicorn

### 🔹 Base de données
- PostgreSQL
- pgvector

### 🔹 Intelligence artificielle
- OpenAI (Embeddings + GPT)
- Architecture RAG

---

## 📁 Structure du projet

```
📦 Projet
├── chat_bot/ # Application Flutter
│ ├── lib/
│ │ ├── api/
│ │ ├── models/
│ │ ├── chat_screen.dart
│ │ └── main.dart
│ └── pubspec.yaml
│
└── RAG_MULTI_MODAL/ # Backend Python
├── api.py
├── rag_core.py
├── ingest.py
├── db.py
├── openai_utils.py
├── data/
│ └── PFE.pdf
└── docker-compose.yml

```
<img width="2387" height="1150" alt="image" src="https://github.com/user-attachments/assets/a6da03f2-94dc-4386-8781-1e0c37263460" />

---

## ⚙️ Fonctionnement du système RAG

1. Le document **PFE.pdf** est découpé en chunks
2. Chaque chunk est transformé en **embedding**
3. Les embeddings sont stockés dans **PostgreSQL (pgvector)**
4. Lors d’une question :
   - Recherche des chunks les plus proches
   - Construction d’un contexte
   - Génération de la réponse avec OpenAI
5. La réponse est envoyée à Flutter via FastAPI

---

## 🚀 Installation & Exécution

### 1️⃣ Lancer PostgreSQL + pgvector
```
docker compose up -d

```

<img width="2004" height="302" alt="image" src="https://github.com/user-attachments/assets/399df23b-5460-4a4b-9018-2c3ccbbd3ce6" />

### 2️⃣ Ingestion du PDF
```
python ingest.py
```
<img width="2024" height="270" alt="image" src="https://github.com/user-attachments/assets/0845d514-d629-421d-a4b4-be8604216105" />

### 3️⃣ Lancer le backend FastAPI
```
python -m uvicorn api:app --reload
```
<img width="2019" height="484" alt="image" src="https://github.com/user-attachments/assets/54ba0582-c79f-4512-8cea-a68d79219a9b" />

### 📍 API disponible sur :

[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

<img width="2540" height="809" alt="image" src="https://github.com/user-attachments/assets/01f287d6-bd58-416d-899f-82430b22d377" />


### 4️⃣ Lancer l’application Flutter
```
flutter run
```

**le chatbot fournit des réponses précises basées sur le contenu du document PDF indexé**

<img width="526" height="1134" alt="image" src="https://github.com/user-attachments/assets/89f56797-5730-4829-bfa1-cb5dc6f6a021" />
<img width="471" height="1022" alt="image" src="https://github.com/user-attachments/assets/4c7bde1e-b01f-401a-9995-eff3eb409304" />

--- 

# ⭐ Conclusion

Ce projet démontre l’intégration complète d’un chatbot intelligent basé sur des documents, en combinant Flutter, FastAPI, PostgreSQL (pgvector) et OpenAI, selon une architecture professionnelle et moderne.










