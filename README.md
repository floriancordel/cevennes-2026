# Cévennes — feuille de route, 9 au 22 août 2026

Carnet de voyage jour par jour, consultable sur téléphone.
Deux bases : Le Vigan (9-15 août) puis Saint-Jean-du-Gard (15-22 août).

## Ce que contient la page

- 14 journées détaillées heure par heure, avec le temps de route de chaque trajet et le total quotidien
- Plafonds tenus : **2h30 de route cumulée par jour, 1h15 maximum d'une seule traite**
- Une seule randonnée par jour, avec la trace GPX correspondante
- Pour chaque lieu : où se garer, les équipements, les restrictions et les pièges connus
- Les repas écrits : note, téléphone cliquable et horaires au restaurant, plat proposé et liste de courses à la maison
- **Altitude et température attendue à l'heure prévue sur chacune des 62 étapes**
- Récapitulatif des réservations à passer, infos pratiques, urgences vétérinaires, réserve d'alternatives

## Comment ça se met à jour

Le fichier est **statique et autonome** : tout le style et tout le code sont à l'intérieur, il n'y a aucune dépendance à installer.

La partie vivante est côté navigateur. À chaque ouverture de la page, un script interroge
[Open-Meteo](https://open-meteo.com/) et remplit les températures :

- **Prévision Météo-France** (modèles AROME 1,3 km et ARPEGE) pour les dates dans la portée des modèles, avec la température à l'heure exacte prévue sur place
- **Projection climatique CMIP6** au-delà de cette portée, en indiquant clairement qu'il s'agit d'un ordre de grandeur et non d'une prévision
- Les températures sont recalées sur l'altitude réelle de chaque lieu, ce qui compte quand une journée passe de 197 m à 1565 m

Plus la date approche, plus d'étapes basculent automatiquement de la projection vers la vraie prévision.
Aucune intervention n'est nécessaire : il suffit de recharger la page.

Un bandeau en haut du document indique combien d'étapes sont en prévision, combien en projection,
et l'heure du dernier relevé.

**Hors ligne**, les altitudes et l'intégralité du carnet restent lisibles ; seules les températures manquent.

## Mettre le contenu à jour

Aucun build, aucune commande. Deux façons de faire :

1. Sur GitHub, ouvrir `index.html`, cliquer sur l'icône crayon, modifier, puis *Commit changes*
2. Ou *Add file* → *Upload files*, déposer une nouvelle version de `index.html`, puis *Commit changes*

GitHub Pages redéploie tout seul en une minute environ.

## Publication

GitHub Pages, branche `main`, dossier racine. Publié sur https://floriancordel.github.io/cevennes-2026/
La page porte une balise `<meta name="robots" content="noindex, nofollow">` : elle n'est pas indexée
par les moteurs de recherche, mais elle reste accessible à toute personne disposant du lien.

## Crédits

Photographies : [Wikimedia Commons](https://commons.wikimedia.org/), sous licences libres
(CC BY-SA, CC BY ou domaine public selon les fichiers). Chaque image renvoie vers sa page source.

Données météo : [Open-Meteo](https://open-meteo.com/), qui redistribue les modèles de Météo-France
et les projections CMIP6.

Sources de l'itinéraire : Parc national des Cévennes, Gard Tourisme, Lozère Tourisme,
Destination Sud Cévennes, Hérault Tourisme, offices de tourisme Cévennes Gorges du Tarn et
Des Cévennes au Mont Lozère, préfectures du Gard et de la Lozère, fichier national des eaux de
baignade, mairies du Vigan, de Saint-Jean-du-Gard, de Val-d'Aigoual, de Florac et de Ganges,
Rando Gard, Visorando, Decathlon Outdoor.
