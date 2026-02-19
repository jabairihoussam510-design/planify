# 🔧 Configuration de l'URL MockAPI

## ⚠️ IMPORTANT : Modifier src/config/api.js

### **Votre URL MockAPI ressemble à :**
```
https://675abc123def456.mockapi.io
```

### **SANS `/api/v1` à la fin !**

---

## ✅ **Configuration CORRECTE**

Ouvrez le fichier `src/config/api.js` et modifiez-le comme ceci :

```javascript
// Configuration MockAPI
// Remplacez par VOTRE URL MockAPI (sans /api/v1)

export const API_URL = 'https://675abc123def456.mockapi.io';

// Endpoints
export const ENDPOINTS = {
  users: `${API_URL}/users`,
  events: `${API_URL}/events`
};
```

---

## 🔍 **Comment trouver votre URL MockAPI ?**

1. Allez sur **https://mockapi.io/projects**
2. Ouvrez votre projet **planify**
3. L'URL est en haut de la page :
   ```
   Project Endpoint: https://675abc123def456.mockapi.io
   ```
4. **Copiez CETTE URL** (sans rien ajouter)

---

## 📝 **Exemple complet**

Si votre URL MockAPI est :
```
https://675d1e2a3456789abc.mockapi.io
```

Alors votre fichier `src/config/api.js` doit être :

```javascript
export const API_URL = 'https://675d1e2a3456789abc.mockapi.io';

export const ENDPOINTS = {
  users: `${API_URL}/users`,
  events: `${API_URL}/events`
};
```

---

## ✅ **Après modification**

1. Sauvegardez le fichier
2. Relancez l'application :
   ```bash
   npm start
   ```
3. Testez l'inscription
4. Si ça marche, poussez sur GitHub :
   ```bash
   git add .
   git commit -m "Configure MockAPI URL"
   git push
   ```

---

## 🧪 **Tester votre API dans le navigateur**

Ouvrez ces URLs dans votre navigateur :

```
https://VOTRE-URL.mockapi.io/users
https://VOTRE-URL.mockapi.io/events
```

Vous devriez voir `[]` (tableau vide)

Si vous voyez une erreur 404, c'est que les ressources n'existent pas sur MockAPI.

---

## 🐛 **Si ça ne marche toujours pas**

Ouvrez la console du navigateur (F12) et regardez les erreurs.

Envoyez-moi :
1. L'URL de votre MockAPI
2. Le message d'erreur dans la console
3. Une capture d'écran de votre projet MockAPI
