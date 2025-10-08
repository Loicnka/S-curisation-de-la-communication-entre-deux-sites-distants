# Securisation-de-la-communication-entre-deux-sites-distants

## contexte 
Projet personnel ayant pour objectif de sécuriser la communication entre deux sites distants (A et B) à l’aide d’un tunnel IPsec site-to-site.
Chaque site dispose d’un pare-feu pfSense et d’un poste client Ubuntu connecté à son réseau local.
Le but est de garantir la confidentialité, l’intégrité et l’authentification des échanges entre les deux réseaux.

## Environnement technique
Systèmes d’exploitation : Ubuntu 22.04 (clients)\
Pare-feux/VPN : pfSense\
Type de VPN : IPsec Site-to-Site\
Protocole : IKEv2 (avec ESP pour le chiffrement)\
Méthode d’authentification : Clé pré-partagée (Pre-Shared Key)\
Chiffrement : AES-256\
Authentification : SHA-256\
Échange de clés : Diffie-Hellman Group 14

## Architecture
<img width="1471" height="533" alt="image" src="https://github.com/user-attachments/assets/31def80f-99fb-47fa-b5b2-3549d5043ab8" />


## Étapes de configuration
### Configuration des interfaces et routes sur pfSense A et B
Affectation des adresses IP LAN/WAN\
Configuration des routes pour atteindre le réseau distant.

### Création du tunnel IPsec sur pfSense
Configuration de la Phase 1 (IKEv2, PSK, AES-256/SHA-256).\
Configuration de la Phase 2 (réseaux locaux et distants).
Ouverture des flux necessaire

### Configuration du pare-feu pour autoriser le trafic IPsec.
Test de connectivité\
Ping du PC A (10.10.1.1) vers PC B (192.168.1.100) via le tunnel.

## Résultat final

Les deux sites distants peuvent communiquer de manière transparente et sécurisée grâce à un tunnel IPsec robuste et chiffré.
Ce projet démontre ma capacité à concevoir, configurer et valider une architecture VPN sécurisée sous environnement open source.

