# Prison

Prison est un jeu d'aventure textuel développé en Python. Le joueur se réveille dans une prison abandonnée et doit trouver comment en sortir en explorant les différentes salles.

Le jeu se joue dans le terminal : on écrit des commandes pour se déplacer, récupérer des objets, discuter avec des personnages et avancer dans les quêtes.

## Lancer le jeu

Il faut avoir Python 3 installé sur son ordinateur. Aucune bibliothèque supplémentaire n'est nécessaire.

1. Télécharger le projet et décompresser le fichier ZIP.
2. Ouvrir un terminal dans le dossier `projetPrison`.
3. Lancer le jeu avec :

```bash
python game.py
```

Sur certains ordinateurs, la commande est `python3 game.py`.

Au démarrage, le jeu demande un nom. Ensuite, il suffit de saisir les commandes dans le terminal.

## Règles du jeu

Le but est de quitter la prison après avoir terminé toutes les quêtes.

- Explorer les salles pour découvrir les lieux et trouver des objets utiles.
- Parler aux personnages : certains donnent des indications pour progresser.
- Récupérer des objets et les utiliser au bon endroit. L'inventaire a une limite de poids.
- Activer les quêtes pour pouvoir remplir leurs objectifs et gagner des points.
- Terminer toutes les quêtes avant d'atteindre la sortie. Sinon, la partie est perdue.

Il faut donc faire attention à ce que l'on ramasse, à l'endroit où l'on dépose les objets et aux indices donnés par les personnages.

## Commandes

| Commande | Utilité |
| --- | --- |
| `help` | Afficher les commandes disponibles |
| `look` | Observer la salle actuelle |
| `go N` | Aller vers le nord |
| `go S` | Aller vers le sud |
| `go E` | Aller vers l'est |
| `go O` | Aller vers l'ouest |
| `go haut` / `go bas` | Monter ou descendre quand c'est possible |
| `back` | Revenir à la salle précédente |
| `history` | Consulter l'historique des déplacements |
| `take objet` | Ramasser un objet présent dans la salle |
| `drop objet` | Déposer un objet de l'inventaire |
| `check` | Voir son inventaire |
| `talk personnage` | Parler à un personnage présent |
| `quests` | Afficher la liste des quêtes |
| `quest titre` | Voir les détails d'une quête |
| `activate titre` | Activer une quête |
| `activate_all_quests` | Activer toutes les quêtes |
| `points` | Consulter son score |
| `rewards` | Voir les récompenses obtenues |
| `quit` | Quitter le jeu |

Les noms des objets, des personnages et des quêtes sont indiqués dans le jeu. Il faut les écrire comme ils apparaissent.

## Exemple de début de partie

```text
Entrez votre nom: Alex
> look
> quests
> activate Explorateur
> go S
> look
```

Pour voir toutes les commandes à n'importe quel moment, on peut taper `help`.

## Organisation du projet

- `game.py` : lancement du jeu, création des salles, personnages et quêtes.
- `actions.py` : commandes disponibles et actions du joueur.
- `player.py` : gestion du joueur, de ses déplacements et de son inventaire.
- `room.py` : gestion des salles et de leurs sorties.
- `item.py` : objets du jeu.
- `character.py` : personnages rencontrés.
- `quest.py` : quêtes, objectifs et récompenses.
- `command.py` : définition des commandes.
- `config.py` : configuration du jeu.

Le projet est réalisé en Python, sans interface graphique.
