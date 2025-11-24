# 🛡️ Cyber-RAG – Assistant Intelligent de Réponse en Cybersécurité

> **Projet de Fin d’Études** – ESPRIT, Tunisie  
> Un système de question-réponse expert en cybersécurité, **sans hallucination**, basé sur Retrieval-Augmented Generation (RAG), NLP avancé et modélisation par graphe (GNN).

---

## 🎯 Objectif

Exploiter un **corpus textuel expert** en cybersécurité pour :
- **Détecter des menaces** et **classifier des incidents** (phishing, malware, vulnérabilités, etc.)
- **Extraire des entités techniques** critiques (CVE, logiciels, techniques MITRE ATT&CK, IPs…)
- Répondre à des questions précises telles que :
  - *« Quelle vulnérabilité affecte Express.js ? »*
  - *« Comment prévenir une attaque SSTI ? »*
  - *« Quels incidents sont liés à la désérialisation non sécurisée ? »*

---

## 🧠 Architecture Technique

- **NLP avancé** :
  - Classification d’incidents de sécurité
  - Extraction d’entités nommées (NER)
  - Embeddings sémantiques avec **Sentence-BERT**
- **Modélisation par graphe** :
  - Construction d’un **graphe hétérogène** (entités ↔ incidents)
  - Application d’un **modèle GNN (HGT)** pour détecter des patterns relationnels entre attaques, vecteurs et cibles
- **Système RAG** :
  - **Retrieval sémantique** via FAISS + Sentence-BERT
  - Aucune génération : les réponses proviennent exclusivement du corpus expert → **zéro hallucination**
- **Interface utilisateur** :
  - Application interactive avec **Gradio**
  - Design épuré, lisible, centré sur la **clarté des réponses techniques**

---

## 🛠️ Technologies Utilisées

- **Langage** : Python  
- **Bibliothèques** : `sentence-transformers`, `FAISS`, `pandas`, `Gradio`, `spaCy`, `NLTK`
- **Modèles** : `all-MiniLM-L6-v2` (embeddings), HGT (GNN en développement/future étape)
- **Données** : Dataset expert en cybersécurité (paires question-réponse techniques)

---

## 📦 Utilisation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/votre-username/cyber-rag.git
   cd cyber-rag
