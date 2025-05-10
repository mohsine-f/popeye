# 🚀 Popeye - DevOps Poll Application

---

## À propos du projet

Ce projet est une **application de sondage temps réel** fournie par l'école, dont l'objectif principal était de **mettre en œuvre une architecture DevOps complète.**

### 🎯 Objectifs pédagogiques

✅ Industrialiser le déploiement d’une application multi-services avec Docker,  
✅ Gérer plusieurs conteneurs interconnectés :  
- Flask (vote),  
- Node.js (résultats),  
- Java Worker,  
- Redis,  
- Postgres,  
✅ Mettre en place une orchestration propre via **Docker Compose**,  
✅ Assurer une communication fiable entre les services (réseaux Docker).

> 🛠 **Note :** Tous les fichiers sources applicatifs ont été fournis ; le cœur du travail portait sur la **mise en place DevOps.**

---

## 🐳 Architecture technique

Le projet est découpé en plusieurs services, chacun **conteneurisé** et orchestré via Docker Compose :

- **Poll (Flask)** ➔ Interface de vote,  
- **Redis** ➔ File d’attente pour stocker les votes,  
- **Worker (Java)** ➔ Traite les votes et les sauvegarde dans la base,  
- **Postgres** ➔ Stockage des votes,  
- **Result (Node.js + Socket.IO)** ➔ Affiche les résultats en temps réel.

Chaque conteneur est connecté à des réseaux **Docker personnalisés** pour assurer l’isolation et la communication sécurisée.

---

## ⚙️ Technologies utilisées

| Service               | Technologie                        |
|-----------------------|------------------------------------|
| Frontend Vote         | Flask (Python)                     |
| Résultats temps réel  | Node.js + Socket.IO                |
| Traitement des votes  | Java (Jedis + JDBC)                |
| Stockage              | Postgres + Redis                   |
| Orchestration         | Docker, Docker Compose             |

---

## 🚦 Schéma d’architecture

<p align="center">
  <img src="assets/popeye-schema.png" alt="Schéma Architecture" width="600">
</p>

---

## 🚀 Lancer le projet

1️⃣ Clone le repo :  
```bash
git clone <repo-url>
cd <repo>
```

2️⃣ Lance la stack complète :

```bash
docker compose up --build
```

3️⃣ Accède à :

* 🗳️ **Vote** ➔ [http://localhost:5000](http://localhost:5000)
* 📊 **Résultats live** ➔ [http://localhost:5001](http://localhost:5001)

---

## 🙌 Contact

💬 Pour toute question ou plus d’infos, contactez-moi ici : [LinkedIn](https://www.linkedin.com/in/mohsine-fajli)

