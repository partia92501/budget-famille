# Budget Famille

Budget familial partagé, hébergé sur GitHub Pages, avec données stockées dans Firebase Firestore et connexion via Google.

## Mise en ligne (GitHub Pages)

1. Sur ce repo : **Settings → Pages**
2. Source : **Deploy from a branch**
3. Branch : **main**, dossier **/(root)**
4. Enregistrer — l'URL sera du type `https://partia92501.github.io/budget-famille/`

## Règles de sécurité Firestore

Le fichier `firestore.rules` contient les règles à coller dans la console Firebase :

Firebase Console → projet **budget-famille** → Firestore Database → onglet **Règles** → coller le contenu de `firestore.rules` → **Publier**.

Ces règles limitent toute lecture/écriture aux comptes Google listés (Emmanuel et Monika). Sans ça, la base reste ouverte à quiconque est connecté.

## Accès

Seuls les comptes Google suivants peuvent se connecter et modifier le budget :
- manulegrand33@gmail.com
- monikalegrand27@gmail.com

Tout autre compte Google est refusé automatiquement (et déconnecté) par la page elle-même, en plus des règles Firestore côté serveur.
