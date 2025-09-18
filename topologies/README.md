# TP Réseaux – Packet Tracer

Ce dépôt contient deux Travaux Pratiques (TP) réalisés avec Cisco Packet Tracer.  
Ils couvrent la configuration de réseaux locaux (LAN), VLAN, routage, serveurs et sécurisation.


# Organisation du dépôt

topologies/
├── 1/ # TP1 : VLAN + Hardening réseau
│ ├── PCs/ # Configurations des postes clients
│ ├── Routeurs/ # Configurations des routeurs
│ ├── serveurs/ # Configurations des serveurs (DNS, Web)
│ ├── switches/ # Configurations des commutateurs

│
├── 2/ # TP2 : Accès Web, DNS, Internet vs VLAN Guest
│ ├── PCs/
│ ├── Routeurs/
│ ├── Serveurs/
│ ├── Switches/
│ ├── topo/ # Fichier Packet Tracer (.pkt)


##  TP1 : VLAN et Hardening Réseau

### Objectifs
- Créer un réseau avec plusieurs VLANs :
  - **VLAN 21 : Direction**
  - **VLAN 22 : Marketing**
  - **VLAN 30 : Services**
  - **VLAN 99 : Guest**
- Mettre en place un **serveur DNS** et un **serveur Web** (intranet).
- Sécuriser l’infrastructure :
  - Interdire Telnet, utiliser SSH.
  - Mettre des mots de passe sur les équipements.
- Empêcher le **VLAN Marketing** et le **VLAN Guest** d’accéder au poste **Direction**.

### Contenu
- Configurations `.config` des **PCs, serveurs, routeurs, switches**.
- Topologie Packet Tracer (`.pkt`).

-------------------------------------------------------------------------------------------

## TP2 : Accès Web, DNS et VLAN Guest

### Objectifs
- Créer un réseau avec deux parties :
  - **LAN interne** (Direction, Services, Marketing, Guest).
  - **Internet simulé** (via un routeur ISP).
- Serveurs :
  - **Web** (intranet, accessible uniquement aux VLAN internes sauf Guest).
  - **DNS**.
- Règles d’accès :
  - Internet **ne peut pas accéder** au serveur Web.
  - Le VLAN **Guest n’a accès qu’à Internet et au DHCP** (pas à l’intranet).

### Contenu
- Configurations `.config` des **PCs, serveurs, routeurs, switches**.
- Fichier topologie **Packet Tracer** (`TP2.pkt`)

##  Utilisation

https://github.com/mkama0/TP

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/mkama0/TP.git
Ouvrir les fichiers .pkt dans Cisco Packet Tracer.

Charger les fichiers .config sur les équipements si nécessaire.



