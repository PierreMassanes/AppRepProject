# UniversalRegistry : Exemples de Clients et Services

_de Chloé Gulielmi & Pierre Massanès_

## Détails de lancement des clients et services

Pour lancer les exemples il faut tout d'abord lancer le serveur http de téléchargement dynamique de classes avec 
les paramètres suivants :

    1098 [chemin vers]/out/production/UniversalRegistryExample
    
Ensuite, chaque main des différents clients et services doivent avoir les arguments de JVM suivants :

    -Djava.rmi.server.useCodebaseOnly=false 
    -Djava.rmi.server.codebase="http://Axxx:1098/" 
    -Djava.security.policy=[Chemin vers policy_server]
    
## Détails de lancement du registre

D'abord il faut lancer un RMI registry au niveau du out/production/UniversalRegistry avec la commande 
    
    rmiregistry -J-Djava.rmi.server.useCodebaseOnly=false 1099

Pour lancer le registre universel, il suffit d'exécuter le main de la classe Server 
et mettre les arguments suivants dans la JVM :

    -Djava.rmi.server.useCodebaseOnly=false -Djava.rmi.server.codebase="http://Axxx:1098/" 
    -Djava.security.policy=[Chemin vers policy_server]

