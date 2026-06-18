# Nostar ✨

Petit logiciel **100 % local** (un seul fichier `index.html`) pour enlever la petite
**étoile** présente sur tes images, proprement, et retrouver toutes tes corrections
dans ton compte.

## Utilisation

1. **Double-clique** sur `index.html` → il s'ouvre dans ton navigateur (Chrome, Edge, Firefox…).
2. Sur l'**écran d'accueil**, clique **Créer un compte** (nom d'utilisateur + email + mot de passe),
   ou **Connexion** (email + mot de passe).
3. Charge ton image : bouton **Ouvrir**, glisser-déposer, ou coller avec `Ctrl+V`.
4. **Marque l'étoile** au **pinceau** (peins en rouge dessus), ou via un bouton de **coin**.
5. Clique **« Retirer l'étoile »** → la zone est reconstruite à partir des pixels voisins.
6. **Enregistre dans ta galerie** (💾) et/ou **télécharge** le résultat en PNG.

Astuce : si une trace reste, repasse le pinceau dessus et reclique « Retirer ».
Le **zoom** aide à viser précisément ; **Effacer la sélection** efface tout le marquage.

## Comptes & galerie « Mes images »

- Connexion par **email** ; le **nom d'utilisateur** est demandé uniquement à la création.
- Chaque compte garde sa propre galerie : **ré-ouvrir**, **re-télécharger** ou **supprimer**
  chaque image (bouton **« 🖼️ Mes images »** en haut à droite).

## Comment fonctionne le retrait

La zone marquée est reconstruite par *inpainting par patchs* (exemplar / Criminisi simplifié) :
Nostar recopie les meilleurs morceaux d'image alentour pour **préserver la texture et les
dégradés**, au lieu de simplement flouter. Si la matière autour est insuffisante, il bascule
sur un remplissage lissé (diffusion).

## Confidentialité

Tout se passe **dans ton navigateur**, sur cet ordinateur. Aucune image n'est envoyée sur
Internet, aucun serveur. Comptes et images sont stockés localement (`localStorage` +
`IndexedDB`). La connexion sert à **organiser tes images localement** — ce n'est pas une
sécurité en ligne, n'y mets pas un mot de passe important. Vider les données du navigateur
efface aussi tes images.

## Fichiers

- `index.html` — l'application (à ouvrir).
- `assets/Logo Nostar.png` — le logo.
