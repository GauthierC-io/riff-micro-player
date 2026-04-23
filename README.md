# Riff Micro-Player

Ce projet est constitué d'une application de démonstration développée sous Clickteam Fusion 2.5, dont la source est commentée ligne par ligne, et d'un tutoriel pour reproduire ce type d'application sous Fusion 2.5.

Il s'agit d'un client radio Shoutcast/Icecast, qui utilise la bibliothèque BASS d'un4seen developments, sous forme de dll.

Pour les besoins de l'exercice, nous utilisons comme exemple la webradio [Riff](https://www.riff-radio.org) qui dispose d'une [API documentée](https://github.com/riffradio/documentation-riff), d'un flux Shoutcast et d'un flux Icecast.

## Fonctionnalités du client

- Prise en charge du flux Icecast et du flux Shoutcast de la webradio Riff
- Affichage de l'artiste et du titre en cours de diffusion
- Utilisation de l'un des points de terminaison de l'API de Riff pour afficher les métadonnées sur le flux Icecast, la webradio ne les diffusant pas directement dans ce flux.
- Vérification de la présence de la DLL au démarrage du client
- Enregistrement des paramètres utilisateur dans la base de registres
- Gestion des erreurs

## Documentation

L'objectif principal de ce projet est de proposer un didacticiel, rédigé à l'attention de la communauté d'utilisateurs de Fusion 2.5. L'application de démonstration a pour objectif principal de servir de support à ce guide. 

Ce document enseigne :

- L'interaction avec une DLL externe via l'extension DLL Object
- L'interaction avec une API via GET Object
- La gestion d'un flux audio Shoutcast/Icecast, y compris le parsing des métadonnées

Veuillez noter que le logiciel présent sur ce dépôt va un peu plus loin que le tutoriel, en offrant une poignée de fonctionnalités supplémentaires.

Le fichier .mfa à ouvrir sous Fusion 2.5, comprend ainsi un commentaire détaillé pour chaque ligne en vue d'en faire un support pédagogique « interactif » supplémentaire.

## Prérequis

- Vous aurez besoin de la bibliothèque [BASS.dll](https://www.un4seen.com/bass.html). Attention, cette bibliothèque est soumise à une licence propriétaire, mais est gratuite pour un usage non-commercial.
- Pour ouvrir le fichier .mfa, vous aurez besoin de Clickteam Fusion 2.5 en édition standard ou supérieure (la Free Edition n'est pas compatible).
- Attention, si Fusion vous indique que l'extension `DLLObject_ANSI.mfx` est introuvable, vous devrez alors copier (ou renommer) votre extension `DLLObject.mfx` sous le nom de `DLLObject_ANSI.mfx` dans les répertoires `Extensions` et `Data\Runtime` de Clickteam Fusion.

## Licences

- Le client en lui-même (exécutable et fichier .MFA) est placé sous licence Mozilla Public License 2.0.
- Le logo Riff utilisé dans le logiciel est la propriété de l'Association Riff. Tous droits réservés.
- La bibliothèque de BASS.dll est la propriété d'un4seen et dispose de sa propre licence propriétaire. Pour en savoir plus, [rendez-vous sur le site d'Un4seen Developments](https://www.un4seen.com/bass.html#license).
