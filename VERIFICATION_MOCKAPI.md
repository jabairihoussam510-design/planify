# ✅ Vérification de votre MockAPI

Votre URL MockAPI est configurée :
```
https://69967af67d178643657442ea.mockapi.io
```

---

## 🧪 **ÉTAPE 1 : Vérifier que vos ressources existent**

### Testez dans votre navigateur :

**Test 1 - Ressource "users" :**
```
https://69967af67d178643657442ea.mockapi.io/users
```

**Test 2 - Ressource "events" :**
```
https://69967af67d178643657442ea.mockapi.io/events
```

### Résultats attendus :

✅ **BON** : Vous voyez `[]` (tableau vide)
✅ **BON** : Vous voyez des données JSON

❌ **MAUVAIS** : Erreur 404 → La ressource n'existe pas
❌ **MAUVAIS** : Page d'erreur → L'URL est incorrecte

---

## 🔧 **ÉTAPE 2 : Si vous voyez une erreur 404**

Cela veut dire que les ressources "users" ou "events" n'existent pas encore.

### Solution :

1. Allez sur **https://mockapi.io/projects**
2. Ouvrez votre projet
3. Créez la ressource **"users"** avec ces champs :
   - `username` (string)
   - `name` (string)
   - `email` (string)
   - `password` (string)

4. Créez la ressource **"events"** avec ces champs :
   - `userId` (string)
   - `day` (string)
   - `title` (string)
   - `time` (string)
   - `room` (string)
   - `color` (string)

---

## 🚀 **ÉTAPE 3 : Lancer votre application**

```bash
# Si l'application tourne déjà, arrêtez-la (Ctrl+C)
npm start
```

---

## ✅ **ÉTAPE 4 : Tester l'inscription**

1. L'application s'ouvre sur `http://localhost:3000`
2. Vous êtes redirigé vers `/login`
3. Cliquez sur **"S'inscrire"**
4. Remplissez :
   - Username : `test123`
   - Nom : `Test User`
   - Email : `test@example.com`
   - Mot de passe : `password123`
   - Confirmer : `password123`
5. Cliquez sur **"S'inscrire"**

### Résultat attendu :
✅ "Compte créé avec succès !"
✅ Redirection vers la page de connexion

---

## 🐛 **Si ça ne marche pas**

### Ouvrez la console du navigateur (F12) :

**Erreur 1 :** `Failed to fetch` ou `Network Error`
→ Vérifiez votre connexion internet

**Erreur 2 :** `404 Not Found` sur `/users`
→ Créez la ressource "users" sur MockAPI

**Erreur 3 :** `CORS error`
→ MockAPI gère CORS automatiquement, vérifiez l'URL

---

## 📸 **ÉTAPE 5 : Vérifier dans MockAPI**

Après avoir créé un compte dans l'application :

1. Retournez sur **https://mockapi.io/projects**
2. Ouvrez votre projet
3. Cliquez sur **"users"**
4. Vous devriez voir votre utilisateur créé :

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

✅ **Si vous voyez ça, tout fonctionne parfaitement !**

---

## 🎯 **Checklist rapide**

- [ ] J'ai testé `https://69967af67d178643657442ea.mockapi.io/users` dans le navigateur
- [ ] Je vois `[]` ou des données (pas d'erreur 404)
- [ ] J'ai testé `https://69967af67d178643657442ea.mockapi.io/events` dans le navigateur
- [ ] Je vois `[]` ou des données (pas d'erreur 404)
- [ ] J'ai relancé l'application (`npm start`)
- [ ] J'ai testé l'inscription
- [ ] Ça fonctionne ! 🎉

---

## 🆘 **Besoin d'aide ?**

Envoyez-moi une capture d'écran de :
1. Ce que vous voyez quand vous ouvrez `https://69967af67d178643657442ea.mockapi.io/users`
2. La console du navigateur (F12) avec l'erreur
3. Votre page MockAPI montrant les ressources

Je vous aide immédiatement ! 😊
