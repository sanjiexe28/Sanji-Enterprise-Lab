
---

# IP Addressing

Plan d'adressage IP de l'infrastructure **Sanji Enterprise Lab**.

---

## Réseau actuel

Le réseau du laboratoire est volontairement séparé du réseau domestique.

| Élément | Valeur |
|---------|--------|
| Réseau | 192.168.0.0/24 |
| Masque | 255.255.255.0 |
| Passerelle | 192.168.0.1 |
| Plage DHCP | À définir |
| DNS | À définir |

---

## Équipements réseau

| Nom | Équipement | Adresse IP | Rôle |
|-----|------------|------------|------|
| RTR-01 | TP-Link TL-WR802N V4 | 192.168.0.1 | Routeur / passerelle |
| SW-01 | TP-Link Omada ES205G | 192.168.0.2 | Switch principal |
| FW-01 | Netgear FVS338 | À définir | Pare-feu |
| SW-02 | HP ProCurve 2910al-24G | À définir | Switch de laboratoire |
| SW-03 | Cisco | À définir | Switch de laboratoire |

---

## Serveurs

| Nom | Adresse IP | Rôle | OS |
|-----|------------|------|----|
| SRV-HV01 | À définir | Hyperviseur Hyper-V | Windows |
| SRV-DC01 | À définir | Contrôleur de domaine / DNS | Windows Server |
| SRV-DC02 | À définir | Contrôleur de domaine secondaire | Windows Server |
| SRV-SUP01 | À définir | Supervision / GLPI | Linux |
| SRV-DB01 | À définir | SGBD | Linux |
| SRV-WEB01 | À définir | Serveur Web | Linux |

Les adresses seront définies au fur et à mesure du déploiement.

---

## Plan VLAN

La segmentation sera mise en place progressivement.

| VLAN | Nom | Réseau | Utilisation |
|------|-----|--------|-------------|
| 10 | Management | À définir | Administration des équipements |
| 20 | Servers | À définir | Serveurs |
| 30 | Users | À définir | Postes utilisateurs |
| 40 | Network | À définir | Équipements réseau |
| 50 | DMZ | À définir | Services exposés |
| 60 | Guest | À définir | Accès invités |
| 99 | Native | À définir | VLAN natif |

> Les réseaux VLAN seront définis avant leur déploiement afin d'éviter les conflits avec le réseau existant.

---

## Règles d'adressage

Les principes suivants sont utilisés :

- Les équipements réseau importants utilisent une adresse IP statique.
- Les serveurs utilisent des adresses IP statiques.
- Les postes clients utilisent principalement DHCP.
- Les plages d'adresses sont organisées par fonction.
- Les réseaux du laboratoire doivent rester distincts du réseau domestique.

---

## Réservations

Les réservations DHCP seront ajoutées ici lorsqu'elles seront mises en place.

| Équipement | Adresse MAC | Adresse IP | Description |
|------------|-------------|------------|-------------|
| À définir | À définir | À définir | À définir |

---

## Historique

| Date | Modification |
|------|--------------|
| 28/06/2026 | Création du plan d'adressage |
| | |
