# Coach Maison – entraînement sans matériel

Application web installable (PWA) de coaching sportif à la maison : séances guidées avec bips et chrono, exercices animés et sourcés (NHS, BHF, ACE, NASM), fréquence cardiaque en Bluetooth (ceinture type Polar H10), marche et course avec GPS, statistiques personnalisables, profils, exports PDF / Excel / CSV / GPX.

## Utiliser l'application
- Adresse (GitHub Pages) : `https://klem38fr.github.io/coach-sport-110VC/`
- Android : ouvrir l'adresse dans **Chrome** → menu ⋮ → **Installer l'application**.
- Bluetooth (FC) et GPS : Chrome ou Edge, page https ; garder l'écran allumé pendant une sortie GPS.

## Mettre à jour
1. Remplacer `index.html` (et `sw.js` si son numéro de version change) dans la branche `main`.
2. GitHub Pages republie automatiquement en 1 à 2 minutes.
3. L'appli installée récupère la nouvelle version à la prochaine ouverture avec internet (le service worker cherche d'abord la version en ligne).

Avant une grosse mise à jour : Paramètres → Profils → **Exporter** (sauvegarde .json de l'historique et des préférences).

## Fichiers
| Fichier | Rôle |
|---|---|
| `index.html` | toute l'application (HTML, CSS, JavaScript) |
| `sw.js` | service worker : fonctionnement hors ligne ; changer `coach-maison-vN` à chaque mise à jour |
| `manifest.webmanifest`, `icon-*.png` | installation sur l'écran d'accueil |

## Données et services externes
- Données personnelles : stockées uniquement dans le navigateur de l'appareil (localStorage), par profil.
- Fonds de carte : © contributeurs OpenStreetMap ; © IGN – Plan IGN et photographies aériennes (Géoplateforme, licence Etalab 2.0).
- Correction du dénivelé : IGN RGE ALTI® (service de calcul altimétrique de la Géoplateforme) en France ; ailleurs Copernicus DEM GLO-90 via Open-Meteo. Les coordonnées de la sortie sont alors envoyées au service choisi.
- Sources des exercices : indiquées sur chaque fiche et dans l'onglet « Sources & conseils ».

Cette application ne remplace pas l'avis d'un médecin ou d'un professionnel du sport.
