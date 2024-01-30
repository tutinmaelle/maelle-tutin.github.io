---
title: "SIO1 AP 6 : Dessiner un schéma réseau et mettre en service un site Web"
date: 2024-01-30T19:53:33+05:30
draft: false
author: "Maelle"
tags:
  - AP 
image: /images/microsoft-visio-2021-logo.jpg
description: ""
toc: true
php: true
---

## I. Présentation du contexte

Née en décembre 2010, la société CUB est une entreprise spécialisée dans l’incubation de startups partageant les mêmes valeurs de solidarité et de développement durable. Au travers de sa plate-forme web, CUB permet à des professionnels d’accéder à des espaces de travail dédiés : salles de réunion, de formation ou de séminaire.

L’entreprise est présente actuellement uniquement à Paris et à Reims et souhaite s’implanter dans de nombreuses autres villes : Lyon, Lille, Montpellier et Strasbourg.

Voici le schéma réseau de l’entreprise actuellement (réalisé avec Microsoft Visio 2021) :

<center><img src="/images/schema_initial.png"></center>


## II. Mission 1 : Les besoins d’adressage

On vous demande de faire évoluer le réseau pour prendre en compte toutes ces villes avec le cahier des charges suivants :

### 1. Cahier des charges 

- Modifier l’adressage IP.
- Ajouter toutes les agences dans le schéma réseau.
- Les adresses IP WANCUB des agences seront de la forme 192.36.253.x0 /24 avec x étant le numéro de l’agence dans l’ordre de numérotation (Reims = 1, Lyon = 2, Lille = 3, …).

### 2. Plan d’organisation de l’activité

<center><img src="/images/Screenshot 2024-01-30 at 10-42-29 SIO1 AP 6 Dessiner un schéma réseau et mettre en service un site Web.png"></center>

## IV. Mission 2 : Evolution du réseau local

L’entreprise CUB a besoin de segmenter le LAN de chaque agence en sous-réseaux pour une question de sécurité. Il est prévu d’affecter chacun de ces sous-réseaux à un VLAN (permet d’utiliser des switchs au lieu de routeurs pour segmenter un réseau).

Le document 1 vous donne la liste des services présents dans le réseau local de chaque agence.

- Vous allez donc devoir modifier le plan d’adressage de chaque agence et faire évoluer le schéma réseau pour qu’il prenne en compte ces changements.
- L’adresse IP du pare-feu dans chaque sous-réseau est la dernière adrese IP disponible.
- Vous choisirez les masques de sous-réseau de manière à avoir la partie hôte du masque la plus petite possible.

<center><img src="/images/Screenshot 2024-01-30 at 10-45-18 SIO1 AP 6 Dessiner un schéma réseau et mettre en service un site Web.png"></center>

## VI. Mission 3 : Héberger un site Web

L’entreprise CUB possède un site Web et souhaite l’héberger dans ses locaux. Vous allez donc devoir mettre en place l’hébergement de ce site sur une machine virtuelle Debian.
