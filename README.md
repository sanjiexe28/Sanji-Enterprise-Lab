# Sanji Enterprise Lab

> Enterprise Systems & Network Administration Laboratory

## Présentation

Sanji Enterprise Lab est un environnement de laboratoire informatique personnel destiné à reproduire une infrastructure d'entreprise.

Le projet a pour objectif de développer et mettre en pratique des compétences en administration systèmes et réseaux dans un environnement contrôlé.

La priorité du projet est l'administration des systèmes et des réseaux. La cybersécurité est abordée comme une compétence complémentaire à travers la sécurisation, la supervision et l'analyse de l'infrastructure.

---

## Objectifs

- Administrer des systèmes Windows et Linux
- Mettre en place une infrastructure réseau
- Administrer des équipements réseau
- Mettre en place Active Directory
- Configurer DNS et DHCP
- Mettre en place une segmentation réseau avec des VLAN
- Administrer un environnement de virtualisation
- Mettre en place une solution de supervision
- Gérer les sauvegardes
- Administrer les accès et les habilitations
- Automatiser certaines tâches d'administration
- Mettre en place des solutions de sécurité réseau
- Documenter les configurations et les interventions

---

## Infrastructure

### Matériel

| Équipement | Rôle |
|------------|------|
| HP EliteBook 840 G5 | Hyperviseur Hyper-V |
| TP-Link TL-WR802N V4 | Accès réseau du laboratoire |
| TP-Link Omada ES205G | Switch principal |
| Netgear FVS338 | Pare-feu |
| HP ProCurve 2910al-24G | Switch de laboratoire |
| Équipements Cisco | Apprentissage réseau |

Le matériel peut évoluer au fur et à mesure du développement du laboratoire.

---

## Virtualisation

L'environnement de simulation d'entreprise utilise **Microsoft Hyper-V**.

Les différentes machines virtuelles seront utilisées pour reproduire les services d'une infrastructure informatique d'entreprise.

Exemples de services prévus :

- Active Directory
- DNS
- DHCP
- Serveurs Windows
- Serveurs Linux
- Supervision
- GLPI
- Base de données
- Services Web
- Sauvegarde

---

## Réseau

Le laboratoire utilise un réseau distinct du réseau domestique afin d'éviter les conflits d'adressage.

Le réseau du laboratoire utilise actuellement :

```text
192.168.0.0/24
