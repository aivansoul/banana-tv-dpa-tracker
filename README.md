# Suivi des DPA fournisseurs — Banana TV

Tableau de bord autonome (un seul fichier HTML, aucune dépendance) pour suivre les accords de
traitement des données (DPA / RGPD art. 28) des 21 fournisseurs de Banana TV.

Pour chaque fournisseur : la démarche exacte à suivre, les liens officiels (DPA, sous-traitants,
trust center, formulaires de signature), un statut, et des notes internes.

## Utilisation

- **Recherche** — la barre de recherche couvre aussi le contenu replié (démarches et intitulés de liens). Raccourci : `/`
- **Statuts** — `À faire`, `En cours`, `En attente fournisseur`, `Terminé`, `Non applicable`. La couleur du statut apparaît sur chaque fiche et dans la barre de progression.
- **Imprimer / PDF** — génère une copie d'archive : toutes les sections dépliées, les URL complètes imprimées à la suite de chaque lien, plus le statut et les notes de chaque fournisseur.
- **Sauvegarder** — export JSON, réimportable via « Restaurer une sauvegarde ».
- **Exporter en CSV** — pour un rapport ou un partage hors ligne.

## Où sont stockées les données

Les statuts et les notes sont enregistrés dans le `localStorage` du navigateur, sur l'appareil
utilisé. **Rien n'est envoyé sur un serveur et rien n'est versionné dans ce dépôt.** Ils ne
suivent donc pas d'un poste ou d'un navigateur à l'autre : exportez une sauvegarde avant de
changer de machine ou de vider le cache du navigateur.

## Technique

- Un fichier, `index.html` : HTML + CSS + JS inline, aucune requête réseau, aucun tracker.
- Thème clair et sombre selon les préférences du système.
- Accessible au clavier, contrastes vérifiés au niveau WCAG AA, `prefers-reduced-motion` respecté.
- Publié via GitHub Pages sur la branche `main`.
