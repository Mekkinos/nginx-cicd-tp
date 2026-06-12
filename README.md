# 🚀 CI/CD Pipeline - Nginx (GitHub Actions)

## 📌 Objectif du projet

Ce projet met en place un pipeline **CI/CD automatisé** permettant de :
- construire une application Nginx dans un conteneur Docker
- vérifier automatiquement la configuration
- garantir la qualité avant exécution

L’objectif est de simuler un workflow réel utilisé en entreprise DevOps.

---

## ⚙️ Niveau 1 - Pipeline CI (Build & Test)

Le pipeline s’exécute automatiquement à chaque :

- push sur la branche `main`
- pull request

### 🔄 Étapes du pipeline :

1. 📥 Récupération du code (Checkout)
2. 📁 Vérification des fichiers essentiels :
   - Dockerfile
   - nginx.conf
   - index.html
3. 🐳 Build de l’image Docker Nginx
4. 🔍 Test de la configuration Nginx (`nginx -t`)
5. ✔ Validation du pipeline

---

## 📊 Schéma du pipeline CI/CD
Push / Pull Request
↓
GitHub Actions
↓
Checkout Code
↓
Check Files
↓
Build Docker Image
↓
Test Nginx Config
↓
✔ Success / ❌ Failure


---

## 🧪 Comportement du pipeline

- ✔ Si tout est correct → pipeline réussi
- ❌ Si une erreur est détectée → pipeline échoue immédiatement
- 🔁 Chaque modification déclenche automatiquement les tests

---

## 🛠️ Technologies utilisées

- 🐳 Docker (containerisation)
- 🌐 Nginx (serveur web)
- ⚙️ GitHub Actions (CI/CD)
- 🐙 Git (versioning)

---

## 🔐 Bonnes pratiques appliquées

- Automatisation des tests
- Validation avant exécution
- Pipeline reproductible
- Isolation via Docker
- Pas de déploiement manuel

---

## 🚀 Résultat

Ce pipeline permet de simuler un processus DevOps réel :
> du code → à un environnement testé et validé automatiquement

---