# GPT Personnalisé pour Haloscan

Ce dépôt fournit un guide et une configuration pour créer un **GPT personnalisé** qui s’intègre avec **Haloscan**, permettant à votre chatbot de récupérer des données SEO et de fournir des recommandations exploitables.

---

## Table des matières

- [Introduction](#introduction)  
- [Prérequis](#prérequis)  
- [Création de votre GPT personnalisé](#création-de-votre-gpt-personnalisé)  
  - [Étape 1 : Remplir les détails du GPT](#étape-1--remplir-les-détails-du-gpt)  
  - [Étape 2 : Configurer les actions](#étape-2--configurer-les-actions)  
  - [Étape 3 : Configurer l’accès au GPT](#étape-3--configurer-laccès-au-gpt)  
  - [Étape 4 : Modifier les paramètres de confidentialité du GPT](#étape-4--modifier-les-paramètres-de-confidentialité-du-gpt)  
- [Actions Haloscan](#actions-haloscan)  
- [Exemples d’appels API](#exemples-dappels-api)  

---

## Introduction

Haloscan est un outil SEO qui fournit des informations sur :

- La performance des sites web  
- Les métriques de mots-clés  
- La visibilité en ligne  

Il aide les utilisateurs à analyser les données et à prendre des décisions SEO éclairées. Ce tutoriel vous guide étape par étape pour créer un **GPT personnalisé** qui s’intègre à Haloscan.

---

## Prérequis

Pour utiliser l’API Haloscan dans votre GPT personnalisé :

### Haloscan

1. Un compte Haloscan valide et une clé API. 
2. Connectez-vous à Haloscan ou inscrivez-vous pour créer un compte.  🎁 Obtenez 8% de réduction avec le code JEREM
3. Obtenez votre clé API : [Cliquez ici](https://tool.haloscan.com/user/api)  
4. Gardez votre clé API confidentielle.

### OpenAI / ChatGPT

1. Un compte ChatGPT avec un **plan Plus** ou **plan Entreprise** (nécessaire pour les GPT personnalisés).  
2. Connectez-vous ou inscrivez-vous.  
3. Créez votre premier GPT : [Cliquez ici](https://chatgpt.com/gpts)  
4. Cliquez sur **+ Créer** pour commencer.

---

## Création de votre GPT personnalisé

### Étape 1 : Remplir les détails du GPT

- **Avatar :** Facultatif  
- **Nom :** par exemple `Assistant SEO Haloscan`  
- **Description :** par exemple `Récupère les données SEO de Haloscan et fournit des recommandations exploitables`  
- Laissez les autres champs vides.

### Étape 2 : Configurer les actions

1. Faites défiler le formulaire jusqu’à **Actions**  
2. Cliquez sur **Créer une nouvelle action**  
3. Authentification :  
   - **Type d’authentification :** API Key  
   - **Clé API :** Votre clé API Haloscan  
   - **Type Auth :** Personnalisé  
   - **Nom de l’en-tête personnalisé :** `haloscan-api-key`  
4. Schéma :   
   - Cliquez sur **Importer de l'URL**  
   - Collez l'URL suivante : https://raw.githubusercontent.com/occirank/Haloscan-openapi/refs/heads/main/keyword-domain.yaml  
   - Cliquez sur **Importer**  
5. Politique de confidentialité : [Copier/collez ce lien](https://www.haloscan.com/privacy/)
   
### Étape 3 : Configurer l’accès au GPT

1. Cliquez sur **Créer**  
2. Choisissez qui peut utiliser le GPT (**Moi uniquement** pour un usage personnel)  
3. Cliquez sur **Enregistrer**  
4. Cliquez sur **Voir GPT** pour vérifier votre GPT nouvellement créé

### Étape 4 : Modifier les paramètres de confidentialité du GPT

- Changez de **Demander** à **Toujours autoriser**

---

## Actions Haloscan

Le GPT inclura une liste d’actions : 

> L’API Haloscan fournit **33 actions**. Chaque fichier OpenAPI peut contenir un maximum de 30 opérations, donc les actions sont réparties sur **deux fichiers OpenAPI**.  
> - Fichier `keyword-domain.yaml` : contient la liste des actions liées aux mots-clés et aux domaines (Keywords Overview, Keywords Match, Domains Overview, etc.)  
> - Fichier `expired-gmb.yaml` : contient les actions liées aux domaines expirés et aux backlinks GMB (Domains Expired, Domains GMB Backlinks, etc.)

### Premier GPT (depuis le premier fichier OpenAPI `keyword-domain.yaml`)

- Crédit utilisateur
- Vue d’ensemble des mots-clés  
- Correspondance des mots-clés  
- Mots-clés similaires  
- Vue d’ensemble des domaines  
- Positions des domaines  
- Pages principales des domaines 

### Deuxième GPT (depuis le deuxième fichier OpenAPI `expired-gmb.yaml`)

- Domaines expirés  
- Révélation des domaines expirés  
- Backlinks GMB des domaines  
- Carte des backlinks GMB  
- Catégories de backlinks GMB  
- Crédit utilisateur

---

## Exemples d’appels API

- Testez votre GPT en envoyant des requêtes simples, comme une URL de site web ou un mot-clé.  
- Le GPT doit retourner des données SEO structurées récupérées depuis l’API Haloscan.

Exemples d’utilisation :

- Tendances de classement des mots-clés  
- Mesures de visibilité des sites web  
- Analyse des concurrents  

Exemple de requête :

```text
"Analyse le mot-clé 'marketing digital' pour monsite.com"
