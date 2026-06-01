# 📱 Classification des SMS — Spam / Ham

> Projet académique — Cours **IFM30513 : Intelligence Artificielle**  
> Professeure : **Nadjate Saïdani** | Automne 2025

---

## 📋 Description du projet

Ce projet implémente un **pipeline complet de classification de messages SMS** permettant de détecter automatiquement les messages indésirables (spam) et les messages légitimes (ham).

Le pipeline combine :
- du **prétraitement textuel** (tokenisation, suppression des stopwords, stemming, TF-IDF)
- une **réduction de dimensionnalité** via un **Autoencoder** (Keras)
- un **modèle de classification** supervisé (régression logistique, SVM, MLP, etc.)

---

## 🗂️ Structure du projet

# Classification-des-SMS-Spam-et-Ham

---

## ⚙️ Pipeline

### 🔹 Étape 1 — Prétraitement des données
- Mise en **minuscule** de tous les textes
- Suppression de la **ponctuation** et des caractères spéciaux
- **Tokenisation** des messages
- Suppression des **stopwords** (mots vides)
- **Stemming** (réduction des mots à leur racine)
- Transformation des messages en **vecteurs TF-IDF**

### 🔹 Étape 2 — Réduction de la dimensionnalité
- Construction d'un **Autoencoder** avec Keras (1 à 3 couches d'encodage)
- Utilisation de **l'espace latent** (couche encodée) comme représentation compressée des données

### 🔹 Étape 3 — Classification
- Application d'un modèle de classification supervisé :
  - Régression Logistique
  - SVM (Support Vector Machine)
  - MLP (Perceptron Multicouches)
- Évaluation sur un jeu de test :
  - ✅ Matrice de confusion
  - ✅ Accuracy, Precision, Recall, F1-score
- Comparaison des performances **avec et sans** réduction de dimensionnalité
- Interprétation des résultats et pistes d'amélioration

---

## 📊 Jeu de données

| Propriété    | Détail                                      |
|-------------|----------------------------------------------|
| Nom         | SMS Spam Collection Dataset                  |
| Source      | UCI Machine Learning Repository              |
| Colonnes    | `label` (spam / ham), `text` (contenu SMS)   |
| Fichier     | `SMSSpamCollection`                          |

---

## 🛠️ Technologies utilisées

| Outil / Bibliothèque | Rôle                            |
|----------------------|---------------------------------|
| Python 3.x           | Langage principal               |
| Pandas / NumPy       | Manipulation des données        |
| NLTK / scikit-learn  | Prétraitement & TF-IDF          |
| Keras / TensorFlow   | Construction de l'Autoencoder   |
| scikit-learn         | Modèles de classification       |
| Matplotlib / Seaborn | Visualisations & métriques      |

---

## 🚀 Installation & Exécution

### 1. Cloner le dépôt
```bash
git clone https://github.com/votre-utilisateur/sms-spam-classifier.git
cd sms-spam-classifier
