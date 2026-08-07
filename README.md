# Cévennes — feuille de route, 9 au 22 août 2026

Carnet de voyage jour par jour, consultable sur téléphone.
Deux bases : Le Vigan (9-15 août) puis Saint-Jean-du-Gard (15-22 août).

## Ce que contient la page

Sept onglets, navigables au pouce sur téléphone et en barre haute sur ordinateur.

**Séjour** — le fil des 14 journées, heure par heure.

- En tête de chaque journée : temps de route, distance et dénivelé de la randonnée, point haut
- Chaque trajet est écrit explicitement : ce qui se termine, où l'on va, l'altitude de départ et
  d'arrivée, la durée, la route empruntée, et un bouton qui lance la navigation
- Plafonds tenus sur les 14 jours : **2h30 de route cumulée, 1h15 maximum d'une seule traite**
- Une seule randonnée par jour, avec la trace Decathlon Outdoor, Visorando ou le GPX direct
- Les jours de changement de lieu commencent par la route : on arrive, on s'installe, et on
  ressort ensuite
- Pour chaque lieu : où se garer, les équipements, les restrictions et les pièges connus
- Les repas écrits : note, téléphone cliquable et horaires au restaurant, plat proposé et liste de
  courses à la maison
- **Altitude et température attendue à l'heure prévue sur chacune des 85 étapes**
- En bas de chaque journée, un bloc **« Si vous avez le temps, ou l'envie »** : une trentaine
  d'idées bonus, rattachées géographiquement à la route du jour, avec leur lien de trace

**Temps forts** — les huit moments qui donnent le ton du séjour, chacun renvoyant à sa journée.

**Carte** — les étapes de chaque journée sur fond OpenStreetMap, semaine par semaine, avec les
points hors programme à portée.

**Tables** — les 21 repas dans l'ordre chronologique, avec en tête le récapitulatif des tables à
réserver (niveau, téléphone cliquable), puis une fiche par repas : photos quand elles existent,
note, avis, horaires, prix, chien, description, alertes.

- **Aucune table en dessous de 4,5 sur Google**, et la source de chaque note est indiquée
- **Deux à trois replis par repas**, chacun avec sa note, ses horaires et son lien

**Courses** — 7 moments d'achat et 10 soirs de préparation, avec la raison de chaque liste.

**Pratique** et **Réserve** — infos pratiques, urgences vétérinaires, randonnées et baignades de
remplacement.

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

## Ce qui se décide tout seul quand il fait chaud

Chaque journée porte son **point haut réel** et une mention *déplaçable* ou *bloquée*, avec la
raison. Une journée est bloquée par un marché qui ne se déplace pas ou par une réservation ferme.

À partir de la prévision du jour, l'application fait trois choses :

1. Au-delà de **34 °C**, elle ouvre un bandeau rouge en tête de la journée avec le repli en
   altitude correspondant
2. Si la journée est déplaçable, elle cherche dans la même semaine une journée **libre, plus haute
   d'au moins 250 mètres et prévue plus fraîche**, et propose l'échange chiffré, en signalant les
   fermetures que l'échange entraînerait
3. En tête de semaine, elle classe les sept journées de la plus chaude à la plus fraîche avec leur
   point haut en face, et marque en rouge celles qui sont basses un jour brûlant

Quand aucun échange n'est possible, elle le dit et explique pourquoi plutôt que de faire semblant.

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
