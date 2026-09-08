# Coach U12 B1 — Grez HC

PWA autonome : aucune base de données, aucun script Google. Tout est enregistré
sur le téléphone qui l'utilise, donc elle fonctionne sans réseau au bord du terrain.

## Mise en ligne (5 min)

1. Sur github.com, crée un nouveau repository (ex : `coach-u12b1`).
2. Dépose les 5 fichiers : `index.html`, `manifest.json`, `service-worker.js`, `icon-192.png`, `icon-512.png`.
3. Settings > Pages > branche principale, dossier `/ (root)`, Save.
4. Attends 1 à 2 minutes, puis ouvre l'URL (ex : `https://tonpseudo.github.io/coach-u12b1/`).
5. Sur le téléphone, menu du navigateur > **Ajouter à l'écran d'accueil**.

## Première utilisation

- Onglet **Joueurs** > "Coller la liste" : une ligne par joueur.
  Les formats `7 Louis Dupont` et `Louis Dupont` sont reconnus.
- L'interrupteur à droite marque le joueur présent ou absent.
  Un joueur passé en absent est retiré automatiquement des 5 compositions.

## Compos

- 5 compositions indépendantes (renommables : "Début", "Q2", "Fin de match"…).
- Postes disponibles : 1 gardien, 3 défenseurs, 3 milieux, 3 attaquants.
- Maximum 8 joueurs sur le terrain : au-delà, il faut libérer un poste.
- "Copier le texte" met la compo dans le presse-papier, prête à coller dans WhatsApp.

## PC

- 3 schémas d'attaque + 1 de défense, chacun avec ses jetons, ses tracés et ses consignes.
- "Dispositif de base" pose une configuration de départ à ajuster.
- Modes : Déplacer (glisser un jeton), Passe (trait jaune pointillé),
  Course (trait blanc), Gomme (toucher un jeton ou un trait pour le supprimer).
- Un simple appui sur un jeton permet de le renommer, ou de le supprimer en validant à vide.

## Sauvegarde

Les données vivent dans le navigateur du téléphone. Avant de changer d'appareil
ou de vider le cache, utilise **Exporter** dans l'onglet Joueurs, puis **Importer**
sur le nouveau téléphone. C'est aussi le moyen de partager la même liste de joueurs
avec un second coach.

## Mise à jour du code

Après avoir modifié `index.html` sur GitHub, incrémente `CACHE` dans
`service-worker.js` (`grez-coach-v1` -> `v2`) pour forcer le rafraîchissement.
