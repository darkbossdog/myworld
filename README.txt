MYWORLD — PREMIÈRE VERSION PWA

Ce dossier contient une première version de l'application MyWorld.

FONCTIONNALITÉS
- Carte mondiale interactive et pays colorés en vert lorsqu'ils sont visités.
- Ajout par nom de pays.
- Recherche de ville ou région avec identification du pays via OpenStreetMap/Nominatim lorsque la connexion est disponible.
- Les recherches de lieux sont mémorisées sur l'appareil pour les retrouver hors connexion.
- Liste des pays visités, compteur et pourcentage.
- Suppression, export et import d'une sauvegarde JSON.
- Carte géographique mise en cache localement après son premier chargement.

IMPORTANT — INSTALLATION PWA
Une PWA et son service worker nécessitent une origine HTTPS (ou localhost). Ouvrir index.html par double-clic permet de voir le code, mais ne permet pas d'installer la PWA ni d'activer le mode hors connexion complet.

Pour tester sur PC :
1. Publier le contenu de ce dossier sur un hébergement statique HTTPS (par exemple GitHub Pages).
2. Ouvrir l'adresse dans Edge ou Chrome avec Internet lors de la première visite.
3. Attendre le chargement complet de la carte.
4. Installer depuis le bouton « Installer » ou le menu du navigateur.

Pour Android :
1. Ouvrir la même adresse HTTPS dans Chrome.
2. Menu ⋮ > Installer l'application (ou Ajouter à l'écran d'accueil).
3. Ouvrir MyWorld une première fois avec Internet pour mettre en cache l'application et la carte.

DONNÉES ET SYNCHRONISATION
Les pays visités sont stockés localement sur chaque appareil (IndexedDB). Il n'y a pas de compte ni de synchronisation automatique. Utiliser Exporter sur un appareil puis Importer sur l'autre pour transférer la liste.

LIMITES DE CETTE PREMIÈRE VERSION
- La recherche d'un pays fonctionne hors connexion. La recherche de villes et régions s'appuie sur Nominatim lors de la première recherche ; les résultats choisis sont ensuite mémorisés localement. Un lieu jamais recherché ne peut pas être identifié hors connexion dans cette version.
- Les frontières des pays sont issues de datasets/geo-countries et Natural Earth. France métropolitaine et les cinq DROM sont individualisés à partir des unités géographiques Natural Earth.
- La bibliothèque Leaflet et la police sont chargées depuis Internet au premier lancement ; prévoir une première ouverture en ligne.
- Pour l'installation PWA réelle, il faudra publier ce dossier sur une adresse HTTPS.

FICHIERS
index.html, styles.css, app.js, sw.js, manifest.webmanifest, assets/icon.svg
