# Organisation-r-seau-avec-Cisco-Packet-Tracer
Utilisation de Cisco Packet Tracer afin de modéliser un reseau comportant des PC et des switch, et vérification de la bonne communication entre deux PC d'un même réseau.

Ce projet m'a permis de comprendre comment s'organise un réseau et comment communiquent les pc d'un même réseau entre eux.

Pour faire un résumé du projet mais (toutes les étapes sont détaillé dans le fichier pdf ennoncé) :

Lorsqu’on met en service un switch, certaines op´erations sont essentielles.

• Changez le nom du switch

Permet d’identifier clairement l’´equipement dans le r´eseau.

• Prot´eger l’acc`es console

Empˆecher un acc`es phusique non autoris´e.

• Prot´eger l’acc`es distant (VTY)

Permet la gestion `a distance (Telnet ou SSH).

• Prot´eger le mode privil´egi´e

S´ecuriser la commande enable.

• Chiffre les mots de passe

Eviter qu’ils apparaissent en clair dans la configuration. ´

• Configurer une adresse IP de gestion

Donner une adresse au switch (via une interface VLAN). Il n’est pas obligatoire
d’utiliser le VLAN 1, et il est mˆeme recommand´e d’utiliser un autre VLAN pour la
gestion.

Pour vous aider à comprendre comment j'ai fait mon projet, le fichier TP2_reseau donne accès au résultats final et les screens dans le dossier screen sont selon moi les étapes les plus importantes. Avec branchements des équipements, configuration des adresses MAC de chaque équipement, configuration des switch, vérification de la communication intra-équipement notamment en testant dans le cmd prompt d'un PC le ping qu'il a avec un autre PC du même réseau.

🌐 TP Réseaux – VLAN, ARP et Routage

📌 Présentation

TP réalisé en L3 Informatique sur Cisco Packet Tracer pour comprendre les bases des réseaux : segmentation (VLAN), communication locale (ARP) et routage.

⸻

🎯 Objectifs
    •    Configurer des VLAN
    •    Mettre en place un trunk
    •    Comprendre ARP
    •    Configurer le routage entre deux réseaux

⸻

🧩 Topologie
    •    2 switches
    •    Plusieurs PC
    •    1 routeur
    •    2 réseaux : 10.1.0.0/16 et 10.2.0.0/16

⸻

🔧 Étapes

VLAN
    •    VLAN 10 et VLAN 20
    •    Isolation des machines
→ Pas de communication entre VLAN

Trunk
    •    Lien entre switches en 802.1Q
→ Les VLAN circulent entre switches

ARP
    •    Résolution IP → MAC
→ Requête broadcast, réponse unicast

Routage
    •    Configuration du routeur :
    
interface g0/0
ip address 10.1.255.254 255.255.0.0

interface g0/1
ip address 10.2.255.254 255.255.0.0

→ Communication entre réseaux OK via gateway

⸻

📊 Résultats
    •    Ping OK dans un même VLAN
    •    Ping KO entre VLAN sans routeur
    •    Ping OK entre réseaux avec routage

⸻

🧠 Compétences acquises
    •    Segmentation réseau (VLAN)
    •    Fonctionnement ARP
    •    Configuration Cisco CLI
    •    Routage IP

⸻

👤 Auteur

Amin Mezouer – L3 Informatique (UVSQ)
