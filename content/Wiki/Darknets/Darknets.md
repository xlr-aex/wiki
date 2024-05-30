- [Tor](https://fr.wikipedia.org/wiki/Tor_(r%C3%A9seau) "Tor (réseau)")[21](https://fr.wikipedia.org/wiki/Darknet#cite_note-21) est une forme de [mixnet](https://fr.wikipedia.org/wiki/Mix_network "Mix network") développée au début des années 2000 par l'armée américaine. Le réseau rassemble plus de 2 millions d'utilisateurs chaque jour[22](https://fr.wikipedia.org/wiki/Darknet#cite_note-22). Tor permet de surfer anonymement sur le web ouvert et intègre un [darkweb](https://fr.wikipedia.org/wiki/Dark_web "Dark web") très actif. C'est là que se trouvent notamment les principaux marchés noirs, mais on y trouve aussi des sites d'expression politique, des ressources techniques, etc.

- [Freenet](https://fr.wikipedia.org/wiki/Freenet "Freenet")[23](https://fr.wikipedia.org/wiki/Darknet#cite_note-23) propose un écosystème anonyme complet (mails, blogs, messagerie, IRC, web) et intègre un mode [F2F (ami à ami)](https://fr.wikipedia.org/wiki/Ami_%C3%A0_ami "Ami à ami"). Dès l'origine, Freenet a été orienté vers la politique et on y trouve de nombreuses ressources associées.

- [I2P](https://fr.wikipedia.org/wiki/I2P "I2P") se comporte comme un [proxy](https://fr.wikipedia.org/wiki/Proxy "Proxy"). Il intègre un [darkweb](https://fr.wikipedia.org/wiki/Dark_web "Dark web") (les _DeepSites_) et permet l'échange de fichiers, l'édition de blogs et une messagerie anonyme. Il permet également de surfer anonymement sur le web ouvert.

- [GNUnet](https://fr.wikipedia.org/wiki/GNUnet "GNUnet") est le système d'anonymisation proposé par le projet [GNU](https://fr.wikipedia.org/wiki/GNU "GNU"). Il est essentiellement utilisé pour le partage de fichiers.

- [Zeronet](https://fr.wikipedia.org/wiki/ZeroNet "ZeroNet") propose de créer un web ouvert et anonyme à partir d'une technologie inspirée des [Bitcoins](https://fr.wikipedia.org/wiki/Bitcoin "Bitcoin").

- [RetroShare](https://fr.wikipedia.org/wiki/RetroShare "RetroShare") fonctionne d'origine en mode [ami à ami](https://fr.wikipedia.org/wiki/Ami_%C3%A0_ami "Ami à ami"), toutefois il est capable de fonctionner en mode dit Darknet « définition populaire » (c'est-à-dire entre anonymes, à savoir les amis des amis) si l'on y désactive la [DHT](https://fr.wikipedia.org/wiki/Table_de_hachage_distribu%C3%A9e "Table de hachage distribuée") et le « Mode découverte ».


# TOR

Le réseau Tor (The Onion Router) fonctionne en utilisant une série de relais pour anonymiser les communications en ligne. Voici une explication simple de son fonctionnement basée sur les images fournies.
#tor #darknet

## Fonctionnement du réseau Tor
# 1. **Encapsulation en couches (Onion Routing)**
![[Pasted image 20240529201428.png]]
La première image montre comment les données sont encapsulées en plusieurs couches de cryptage, comme des couches d'oignon. Chaque couche est chiffrée avec la clé d'un relais spécifique:
- **Router A Key** (clé du routeur A) en bleu
- **Router B Key** (clé du routeur B) en vert
- **Router C Key** (clé du routeur C) en rouge
Les données sont encapsulées plusieurs fois et chaque relais du réseau Tor enlève une couche de cryptage pour révéler le prochain relais où envoyer les données. Ce processus se répète jusqu'à ce que les données atteignent leur destination finale.
    
    
    
# 2. **Routage à travers le réseau Tor** 


![[Pasted image 20240529201517.png]]

La deuxième image illustre le parcours des données à travers le réseau Tor :

- **Client Tor** : Le point de départ des données.
- **Entry Guard** : Le premier relais, qui enlève la première couche de cryptage.
- **Middle Relay** : Le relais intermédiaire, qui enlève la deuxième couche de cryptage.
- **Exit Relay** : Le relais final, qui enlève la dernière couche de cryptage et envoie les données à la destination.

Les données sont chiffrées tout au long de leur parcours dans le réseau Tor, sauf lors de leur sortie par l'Exit Relay. Cela garantit que ni les intermédiaires ni les observateurs extérieurs ne peuvent retracer le chemin des données jusqu'à leur origine ou destination.
#onion-routing #routing

# 3. **Les nœuds au sein de Tor**
### **Les Onion Routers (OR) ou relais**

Les Onion Routers, souvent appelés relais, sont les nœuds fondamentaux du réseau Tor. Ils constituent les circuits par lesquels transitent les paquets de données à travers le réseau. Leur fonction principale est de recevoir des données chiffrées, de les décrypter partiellement, et de les transmettre au prochain relais dans le circuit, en répétant ce processus jusqu'à ce que les données atteignent leur destination finale. Chaque relais ne connaît que le relais précédent et le relais suivant, ce qui permet de garantir qu'aucun relais individuel ne peut retracer le chemin complet d'une communication source.

### **Les Nœuds clients ou Onions Proxies (OP)**

Les nœuds clients, également appelés onions proxies (par abus de langage), sont les points d'entrée pour les utilisateurs dans le réseau Tor. Ces nœuds représentent les clients logiciels Tor installés sur les dispositifs des utilisateurs. Leur rôle est d'initier les connexions vers le réseau Tor en construisant un circuit à travers plusieurs relais (OR) pour garantir l'anonymat. Le nœud client choisit aléatoirement plusieurs relais pour créer un chemin sécurisé à travers le réseau, et chiffre les données de manière à ce que chaque relais ne puisse décrypter que sa propre couche d'encapsulation, une technique connue sous le nom de routage en oignon source.

### **Les Directory Servers ou Authority Servers**

Les Directory Servers, également appelés authority servers, sont les nœuds qui maintiennent une liste à jour des Onion Routers disponibles et fiables. Ils jouent le rôle d'annuaires du réseau Tor. Lorsqu'un nœud client veut se connecter au réseau, il consulte ces serveurs pour obtenir une liste des relais qu'il peut utiliser pour construire son circuit. Les Directory Servers sont cruciaux pour le bon fonctionnement de Tor car ils fournissent les informations nécessaires pour que les clients puissent choisir des relais fiables et éviter ceux qui pourraient être compromis ou malveillants source.
#nodes 

# I2P
Le réseau I2P (Invisible Internet Project) est un réseau anonyme conçu pour protéger la confidentialité des communications en ligne. Voici une explication simple de son fonctionnement, basée sur les concepts et le fonctionnement de Tor pour mieux comprendre les différences et les similarités.

## Fonctionnement du réseau I2P

### 1. **Encapsulation en couches (Garlic Routing)**

![[Pasted image 20240529204406.png]] La première image montre comment les données sont encapsulées en plusieurs couches de cryptage, similaire au routage en oignon de Tor, mais avec des différences importantes. I2P utilise le "Garlic Routing" où plusieurs messages (ou "gousses d'ail") sont encapsulés ensemble pour augmenter l'anonymat et l'efficacité :

- **Packet** (Paquet) : Représente l'ensemble des messages chiffrés ensemble.
- **Message** (Message) : Les unités de données individuelles encapsulées dans le paquet.
- **Router** (Routeur) : Les nœuds du réseau I2P par lesquels les paquets transitent.

Chaque couche est chiffrée avec la clé d'un nœud spécifique. Les données sont encapsulées plusieurs fois et chaque nœud du réseau I2P enlève une couche de cryptage pour révéler le prochain nœud où envoyer les données. Ce processus se répète jusqu'à ce que les données atteignent leur destination finale.

## 2. **Routage à travers le réseau I2P**

![[Pasted image 20240529204901.png]] 
La deuxième image illustre le parcours des données à travers le réseau I2P :

- **Client I2P** : Le point de départ des données.
- **Inbound Gateway** : Le premier nœud d'entrée, qui enlève la première couche de cryptage.
- **Outbound Tunnel** : Le tunnel de sortie, qui est utilisé pour transmettre les données hors du réseau I2P.
- **Outbound Endpoint** : Le dernier nœud de sortie, qui enlève la dernière couche de cryptage et envoie les données à la destination.

Les données sont chiffrées tout au long de leur parcours dans le réseau I2P, ce qui garantit que ni les intermédiaires ni les observateurs extérieurs ne peuvent retracer le chemin des données jusqu'à leur origine ou destination.

## 3. **Les nœuds au sein de I2P**

### **Les Routers I2P**

Les routers I2P sont les nœuds fondamentaux du réseau I2P. Ils constituent les circuits par lesquels transitent les paquets de données à travers le réseau. Leur fonction principale est de recevoir des données chiffrées, de les décrypter partiellement, et de les transmettre au prochain nœud dans le circuit, en répétant ce processus jusqu'à ce que les données atteignent leur destination finale. Chaque nœud ne connaît que le nœud précédent et le nœud suivant, ce qui permet de garantir qu'aucun nœud individuel ne peut retracer le chemin complet d'une communication source.

### **Les Nœuds clients (Client Tunnels)**

Les nœuds clients, ou client tunnels, sont les points d'entrée pour les utilisateurs dans le réseau I2P. Ces nœuds représentent les logiciels I2P installés sur les dispositifs des utilisateurs. Leur rôle est d'initier les connexions vers le réseau I2P en construisant un circuit à travers plusieurs routers (I2P Routers) pour garantir l'anonymat. Le nœud client choisit aléatoirement plusieurs routers pour créer un chemin sécurisé à travers le réseau, et chiffre les données de manière à ce que chaque router ne puisse décrypter que sa propre couche d'encapsulation, une technique similaire au routage en oignon mais adaptée au Garlic Routing source.

### **Les Réseaux de Répartition (Floodfill Routers)**

Les Floodfill Routers sont des nœuds spécialisés qui maintiennent une liste à jour des I2P Routers disponibles et fiables. Ils jouent le rôle d'annuaires du réseau I2P. Lorsqu'un nœud client veut se connecter au réseau, il consulte ces nœuds pour obtenir une liste des routers qu'il peut utiliser pour construire son circuit. Les Floodfill Routers sont cruciaux pour le bon fonctionnement de I2P car ils fournissent les informations nécessaires pour que les clients puissent choisir des routers fiables et éviter ceux qui pourraient être compromis ou malveillants source.

### 4. **Diagramme de communication dans I2P**

La troisième image montre un exemple de communication dans le réseau I2P, impliquant plusieurs utilisateurs (Alice, Bob, Charlie, Dave) et la manière dont les tunnels sont utilisés :

- **Alice** : L'utilisateur initiateur de la communication.
- **Tunnels Inbound et Outbound** : Les chemins utilisés pour envoyer et recevoir des données. Les tunnels verts représentent les tunnels entrants (inbound), et les tunnels roses représentent les tunnels sortants (outbound).
- **Destinations et Gateways** : Les points de terminaison et les passerelles pour chaque segment de tunnel.
- **Routers Locaux** : Les nœuds locaux qui relaient les données entre les différents segments de tunnel.

Chaque tunnel est sécurisé et utilise des couches de cryptage pour garantir l'anonymat et la confidentialité des communications.