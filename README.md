# Discord-boy

## _Une version forked du bot Discord Sblerboy_

Discord-boy est un bot Discord permettant de jouer à des jeux de Gameboy directement dans Discord.

## Fonctionnalité

- Permet de jouer à des jeux de Gameboy dans un salon dédié
- Enregistre les différentes actions des joueurs dans un salon de logs

## Principe de fonctionnement

- Les utilisateurs réagissent au message principal pour faire avancer le jeu. Il est possible de changer "l'objectif actuel" en changeant la description du salon de jeu.

![alt text](https://cdn.discordpp.com/attachments/849667753295347745/874205955196346418/unknown.png)

- Quand un joueur réagit, son action est envoyée dans le salon de logs

![alt text](https://cdn.discordpp.com/attachments/849667753295347745/874206021818675240/unknown.png)

## Pré-requis

- Une installation de python 3 fonctionnelle
- Un serveur Discord dont vous êtes l'admin et qui possède au moins 3 salons textuels.
- Un de ces salons doit être réservé au bot, il doit être le seul à pouvoir envoyer des messages dedans. Il doit aussi être le seul à pouvoir ajouter des réactions aux messages dans ce salon.
- Un bot Discord dont vous êtes le créateur. Il doit avoir les 3 [intents d'activés](https://discord.com/developers/docs/topics/gateway#enabling-privileged-intents).
- Une rom de jeu de gameboy au format .gb

## Installation

- Cloner le repo

```sh
git clone https://github.com/MartinTech63/Discord-boy.git
```

- Installer les libraires

```sh
cd Discord-boy
pip install -r requirements.txt
```

- Remplir le fichier config.ini avec les valeurs qui correspondent à votre cas d'utilisation

  - ID_CHANNEL correspond à l'ID du salon textuel dans lequel le bot va envoyer son message pour que les joueurs réagissent
  - ID_GUILD correspond à l'ID du serveur Discord dans lequel le bot va opérer
  - ID_LOG_CHANNEL correspond à l'ID du salon textuel dans lequel le bot va envoyer les différentes actions enregistrées
  - ID_CHAT_CHANNEL correspond à l'ID du salon textuel dans lequel vous souhaitez que les joueurs discutent du jeu
  - BOT_TOKEN est le token de votre bot Discord

- Renommer votre rom en "rom.gb" et la placer dans le répertoire "rom"

- Lancer le bot

```sh
python3 discord-boy.py
```

## License

GNU General Public License (GPL)
