# 📸 Guide VISUEL - Configuration MockAPI (Étape par Étape)

## 🎯 Objectif : Créer votre base de données gratuite en 5 minutes

---

## 📝 **ÉTAPE 1 : Créer un compte MockAPI**

### Action :
1. Ouvrez votre navigateur
2. Allez sur **https://mockapi.io/**
3. Cliquez sur le bouton **"Get Started Free"** (en haut à droite)
4. Choisissez votre méthode de connexion :
   - 🐙 **Continue with GitHub** (recommandé)
   - 🔵 **Continue with Google**
   - 📧 **Sign up with Email**

### Résultat :
✅ Vous arrivez sur le **Dashboard MockAPI**

---

## 📁 **ÉTAPE 2 : Créer un projet**

### Action :
1. Sur le dashboard, cliquez sur **"+ New Project"**
2. Une popup s'ouvre
3. Remplissez :
   - **Project Name** : `planify`
4. Cliquez sur **"Create"**

### Résultat :
✅ Votre projet "planify" est créé
✅ Vous voyez l'URL de votre projet en haut :
```
Project Endpoint: https://675abc123def456.mockapi.io
```

**⚠️ COPIEZ CETTE URL QUELQUE PART !**

---

## 👥 **ÉTAPE 3 : Créer la ressource "users"**

### Action :
1. Dans votre projet, cliquez sur **"+ New Resource"**
2. Une popup s'ouvre
3. Remplissez :
   - **Resource name** : `users` (tout en minuscules)
4. Cliquez sur **"Create"**

### Résultat :
✅ La ressource "users" est créée
✅ Vous voyez une page avec un tableau vide

---

## ⚙️ **ÉTAPE 4 : Ajouter les champs à "users"**

### Action :
1. Sur la page de la ressource "users"
2. Vous voyez le champ **"id"** déjà présent (gardez-le)
3. Cliquez sur **"+ New Field"** ou **"Add field"**
4. Ajoutez ces champs UN PAR UN :

#### Champ 1 :
- **Field name** : `username`
- **Type** : String
- Cliquez sur ✅ pour valider

#### Champ 2 :
- **Field name** : `name`
- **Type** : String
- Cliquez sur ✅

#### Champ 3 :
- **Field name** : `email`
- **Type** : String
- Cliquez sur ✅

#### Champ 4 :
- **Field name** : `password`
- **Type** : String
- Cliquez sur ✅

### Résultat :
✅ Vous avez maintenant 5 champs dans "users" :
```
id (number) - auto-généré
username (string)
name (string)
email (string)
password (string)
```

---

## 📅 **ÉTAPE 5 : Créer la ressource "events"**

### Action :
1. Cliquez sur le nom du projet en haut à gauche pour revenir au menu
2. Cliquez à nouveau sur **"+ New Resource"**
3. Remplissez :
   - **Resource name** : `events` (tout en minuscules)
4. Cliquez sur **"Create"**

### Résultat :
✅ La ressource "events" est créée

---

## ⚙️ **ÉTAPE 6 : Ajouter les champs à "events"**

### Action :
Ajoutez ces champs UN PAR UN :

#### Champ 1 :
- **Field name** : `userId`
- **Type** : String

#### Champ 2 :
- **Field name** : `day`
- **Type** : String

#### Champ 3 :
- **Field name** : `title`
- **Type** : String

#### Champ 4 :
- **Field name** : `time`
- **Type** : String

#### Champ 5 :
- **Field name** : `room`
- **Type** : String

#### Champ 6 :
- **Field name** : `color`
- **Type** : String

### Résultat :
✅ Vous avez maintenant 7 champs dans "events" :
```
id (number) - auto-généré
userId (string)
day (string)
title (string)
time (string)
room (string)
color (string)
```

---

## 🧪 **ÉTAPE 7 : Tester votre API**

### Action :
1. Copiez votre URL de projet (en haut de la page)
2. Ouvrez un nouvel onglet dans votre navigateur
3. Collez l'URL et ajoutez `/users` :
   ```
   https://VOTRE-URL.mockapi.io/users
   ```
4. Appuyez sur Entrée

### Résultat attendu :
```json
[]
```
(Un tableau vide - c'est NORMAL et c'est BON !)

### Si vous voyez une erreur :
❌ **404 Not Found** → La ressource "users" n'existe pas
❌ **Invalid URL** → L'URL est incorrecte

---

## 💻 **ÉTAPE 8 : Configurer votre code React**

### Action :
1. Ouvrez votre projet PLANIFY dans un éditeur de code
2. Ouvrez le fichier `src/config/api.js`
3. Remplacez l'URL par défaut par VOTRE URL :

**AVANT :**
```javascript
export const API_URL = 'https://your-project-id.mockapi.io/api/v1';
```

**APRÈS (REMPLACEZ par votre URL) :**
```javascript
export const API_URL = 'https://675abc123def456.mockapi.io';
```

⚠️ **ATTENTION : PAS de `/api/v1` à la fin !**

### Le fichier complet doit ressembler à :
```javascript
// Configuration MockAPI
export const API_URL = 'https://675abc123def456.mockapi.io';

// Endpoints
export const ENDPOINTS = {
  users: `${API_URL}/users`,
  events: `${API_URL}/events`
};
```

4. **Sauvegardez le fichier** (Ctrl+S ou Cmd+S)

---

## 🚀 **ÉTAPE 9 : Tester l'application**

### Action :
```bash
# Si l'application tourne déjà, arrêtez-la (Ctrl+C)
# Puis relancez :
npm start
```

### Test :
1. L'application s'ouvre sur `http://localhost:3000`
2. Vous êtes redirigé vers `/login`
3. Cliquez sur **"S'inscrire"**
4. Remplissez le formulaire :
   - Username : `test123`
   - Nom : `Test User`
   - Email : `test@example.com`
   - Mot de passe : `password123`
   - Confirmer : `password123`
5. Cliquez sur **"S'inscrire"**

### Résultat attendu :
✅ Message : "Compte créé avec succès !"
✅ Redirection vers la page de connexion

### Si erreur :
❌ Ouvrez la console du navigateur (F12)
❌ Regardez le message d'erreur
❌ Vérifiez que l'URL dans `api.js` est correcte

---

## ✅ **ÉTAPE 10 : Vérifier dans MockAPI**

### Action :
1. Retournez sur **https://mockapi.io/projects**
2. Ouvrez votre projet **planify**
3. Cliquez sur la ressource **"users"**

### Résultat attendu :
✅ Vous voyez votre utilisateur créé :
```json
[
  {
    "id": "1",
    "username": "test123",
    "name": "Test User",
    "email": "test@example.com",
    "password": "password123"
  }
]
```

**Si vous voyez ça, TOUT FONCTIONNE ! 🎉**

---

## 🎉 **FÉLICITATIONS !**

Votre MockAPI est configurée et fonctionne !

Vous pouvez maintenant :
- ✅ Vous inscrire
- ✅ Vous connecter
- ✅ Ajouter des événements
- ✅ Modifier des événements
- ✅ Supprimer des événements

---

## 🐛 **Problèmes courants**

### Problème 1 : "Failed to fetch"
**Cause** : URL incorrecte dans `api.js`
**Solution** : Vérifiez l'URL, pas de `/api/v1`

### Problème 2 : "404 Not Found"
**Cause** : Ressources "users" ou "events" n'existent pas
**Solution** : Créez-les sur MockAPI

### Problème 3 : "CORS error"
**Cause** : MockAPI devrait gérer CORS automatiquement
**Solution** : Vérifiez que l'URL est exacte

### Problème 4 : Rien ne se passe
**Cause** : Fichier `api.js` pas sauvegardé ou app pas relancée
**Solution** : Sauvegardez et faites `npm start`

---

## 📞 **Besoin d'aide ?**

Envoyez-moi :
1. **Votre URL MockAPI** (ex: https://675abc.mockapi.io)
2. **Le message d'erreur** dans la console (F12)
3. **Une capture d'écran** de votre projet MockAPI

Je vous aide immédiatement ! 😊
