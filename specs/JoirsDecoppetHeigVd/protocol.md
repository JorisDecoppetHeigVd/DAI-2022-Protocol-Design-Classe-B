# Spécificité du protocole
## Que fait le protocole
Il premet à un client de demander un calcul au serveur.


Le serveur retourne le résultat du caulcul.
## Fonctionnement général
### Protocol de transport utilisé
TCP, il est important que la demande et la réponse arrivent bien à destination.
### Comment le client trouve le serveur
Grâce à son nom et son numéro de port.
### Qui parle en premier
Le client avec une demande de discution.
### Qui termine la discution et quand
Le serveur avec une validation de fin de discution.
## Message
### Quelle est la syntaxe des messages
"signe";"nombre 1";"nombre 2"
### Quelle est la séquence des messages
- client SYN
- server SYN/ACK
- client ACK
- client Data
- server ACK
- server DATA
- client ACK
- server FIN
- client FIN/ACK
- server ACK

En résumé, client envoye le calcul puis le serveur envoie la réponse.
### Que se passe-t-il quand un message est reçu
#### Client
Il affiche le résultat retourné.
#### Serveur
Il transforme la string en calcul puis le traite.
## Elements spéciques
### Opération supportée
multiplication, division, addition et soustraction
### Gestion des erreurs
lorsque le signe n'est pas suportée, qu'il manque un nombre ou que les noubres ne soit pas un nombre. Un message d'erreur est retourné.
### Extension
Pouvoir avoir des calculs plus long
## Exemples

