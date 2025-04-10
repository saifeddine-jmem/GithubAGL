# 🎮 Boutique Jeux en Ligne

## 🧑‍💻 Auteurs
- Nessim Hjaiej  
- Seifeddine Jmem  
- Wassim Guidara  

📅 **Date** : 07/04/2025

---

## 📌 1. Introduction au projet

Ce projet a pour objectif de développer une application Java représentant une **boutique en ligne** permettant l’achat de jeux vidéo.  
L’application propose :
- une interface graphique conviviale pour les **clients**
- un panneau de gestion pour les **administrateurs**

🔧 Ce projet applique :
- les **principes de conception orientée objet**
- la **modélisation UML**
- la **gestion d’interfaces utilisateur**

---

## 📋 2. Spécification du projet

### 👥 Fonctionnalités côté client :
- S’inscrire / Se connecter
- Parcourir les jeux
- Rechercher un jeu
- Consulter les détails
- Ajouter au panier
- Modifier le panier
- Passer à la caisse

### 🛠️ Fonctionnalités côté administrateur :
- Se connecter
- Gérer les utilisateurs
- Gérer le catalogue de jeux

💡 Les données sont **stockées en mémoire** (pas de base de données).

---

## 📈 3. Diagramme de cas d’utilisation

> Le diagramme est fourni séparément dans le rendu du projet.

---

## 🚀 4. Sprint 1 - Cas d'utilisation prioritaires

- ✅ S’inscrire / Se connecter  
- ✅ Ajouter un jeu au panier

### 🔁 Méthodologie :
- Identification des cas d'utilisation prioritaires
- Définition des préconditions / postconditions
- Préparation de **tests de validation** (table de décision)

---

## 🧪 Spécification - Cas : S'inscrire / Se connecter

- **Précondition** : L'utilisateur a accès à l'application
- **Postcondition** : Connexion réussie ou message d’erreur
- **Entrée** : Email, mot de passe, nom complet (si inscription)
- **Retour** :
  - ✅ Connexion / inscription réussie → accès tableau de bord
  - ❌ Échec → message d’erreur

### Table de décision :

| Email valide | Mot de passe valide | Utilisateur existant | Résultat |
|--------------|---------------------|-----------------------|----------|
| F            | -                   | -                     | ❌       |
| T            | F                   | -                     | ❌       |
| T            | T                   | F                     | ✅       |
| T            | T                   | T                     | ✅ / ❌  |

---

## 🛒 Spécification - Cas : Ajouter un jeu au panier

- **Précondition** : L'utilisateur est connecté et accède à la liste des jeux
- **Postcondition** : Jeu ajouté ou ignoré
- **Entrée** : Nom du jeu, identifiant utilisateur (session)
- **Retour** :
  - ✅ Ajout réussi → “Jeu ajouté au panier”
  - ⚠️ Déjà présent → “Ce jeu est déjà dans votre panier”
  - ❌ Aucun jeu sélectionné → “Veuillez sélectionner un jeu”

### Table de décision :

| Jeu sélectionné | Déjà dans le panier | Résultat |
|------------------|----------------------|----------|
| ❌               | -                    | ❌       |
| ✅               | ✅                   | ❌       |
| ✅               | ❌                   | ✅       |
