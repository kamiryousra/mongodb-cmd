# MongoDB CRUD Checkpoint

## 📌 Description
Ce projet contient les commandes et captures d’écran réalisées pour pratiquer les opérations CRUD (Create, Read, Update, Delete) avec MongoDB en utilisant `mongosh`.

## 🗄️ Base de données et collection
- **Database** : `contact`
- **Collection** : `contactlist`

## 📥 Données insérées
```json
[
  { "lastName": "Ben", "firstName": "Moris", "email": "ben@gmail.com", "age": 26 },
  { "lastName": "Kefi", "firstName": "Seif", "email": "kefi@gmail.com", "age": 15 },
  { "lastName": "Emilie", "firstName": "Brouge", "email": "emilie.b@gmail.com", "age": 40 },
  { "lastName": "Alex", "firstName": "Brown", "age": 4 },
  { "lastName": "Denzel", "firstName": "Washington", "age": 3 }
]
✅ Opérations effectuées
Afficher toute la liste des contacts


Copier le code
db.contactlist.find()
Afficher un contact par son ID


Copier le code
db.contactlist.find({ _id: ObjectId("...") })
Afficher tous les contacts avec age > 18

js
Copier le code
db.contactlist.find({ age: { $gt: 18 } })
Afficher tous les contacts avec age > 18 et name contenant "ah"


Copier le code
db.contactlist.find({ age: { $gt: 18 }, firstName: /ah/i })
Modifier un prénom ("Seif" → "Anis")


Copier le code
db.contactlist.updateOne(
  { lastName: "Kefi", firstName: "Seif" },
  { $set: { firstName: "Anis" } }
)
Supprimer les contacts avec age < 5


Copier le code
db.contactlist.deleteMany({ age: { $lt: 5 } })
Afficher la liste finale


Copier le code
db.contactlist.find()
📸 Captures d’écran
Toutes les étapes ont été sauvegardées en captures d’écran pour validation.


---

👉 Veux-tu que je te génère aussi un **README plus court (1 page max, type rapport PDF)** que tu peux donner directement comme rendu avec tes screenshots ?











ChatGPT peut faire des erreurs. Envisagez de vérifier les infor
