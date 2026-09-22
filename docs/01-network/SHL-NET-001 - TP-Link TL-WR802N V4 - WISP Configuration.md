# SHL-NET-001 - Configuration du TP-Link TL-WR802N V4 en mode WISP

---

## 01 - Informations du document

| Champ | Valeur |
|---|---|
| Document ID | SHL-NET-001 |
| Titre | Configuration du TP-Link TL-WR802N V4 en mode WISP |
| Catégorie | Réseau |
| Criticité | Moyenne |
| Temps estimé | 15 min |
| Version | 1.0 |
| Statut | Validé |
| Auteur | Sanjiexe |
| Date de création | 28/06/2026 |
| Dernière mise à jour | 28/06/2026 |
| Tags | TP-Link, WR802N, Wi-Fi, Ethernet, WISP |

---

## 02 - Objectif

Configurer le TP-Link TL-WR802N V4 en mode **WISP** afin de récupérer la connexion Wi-Fi de la box et de la transmettre en Ethernet vers le switch **SW-01**.

Cette configuration permet de connecter l'infrastructure du laboratoire sans avoir besoin de relier directement le switch à la box Internet.

---

## 03 - Contexte

L'infrastructure du laboratoire ne peut pas être reliée directement à la box avec un câble Ethernet.

Le TP-Link TL-WR802N V4 sert donc de point d'accès au réseau Wi-Fi existant. Il récupère la connexion Wi-Fi et la fournit en Ethernet au switch **SW-01**.

Le réseau du laboratoire est séparé du réseau domestique. Le réseau du laboratoire utilise actuellement le réseau `192.168.0.0/24`

---

## 03.5 - Prérequis

- TP-Link TL-WR802N V4 alimenté en 5 V / 1 A
- Poste d'administration
- Câble Ethernet RJ45
- Accès au réseau Wi-Fi de la box
- SSID du réseau Wi-Fi
- Mot de passe Wi-Fi
- Navigateur web
- Accès à l'interface d'administration du WR802N

---

## 04 - Matériel utilisé

| Composant | Rôle | IP / FQDN | OS / Version |
|---|---|---|---|
| TP-Link TL-WR802N V4 | Routeur WISP / accès au réseau | 192.168.0.1 | Firmware TP-Link |
| Box Internet | Fournit l'accès Internet et le Wi-Fi | 192.168.1.0/24 | Firmware FAI |
| PC d'administration | Configuration du WR802N | DHCP | Windows 11 |
| TP-Link Omada ES205G | Switch principal du laboratoire | 192.168.0.2 | Firmware TP-Link |

---

## 05 - Schéma réseau

```text
                    Internet
                        │
                       Box 
                  192.168.1.0/24
                        │
                      Wi-Fi
                        │
                RTR-01 / WR802N
                   Mode WISP
                  192.168.0.1
                        │
                    Ethernet
                        │
                 SW-01 / ES205G
                        │
              ┌─────────┼─────────┐
              │         │         │
            FW-01    SRV-HV01   Cisco
