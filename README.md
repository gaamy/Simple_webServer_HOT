# Simple_webServer_HOT
Implementation of a simple Heat Openstack Template(HOT) to deploy a python web server on the cloud.

Déploiement d'un service Web sur une seule machine virtuelle

Vous devez créer un gabarit Heat permettant de déployer le serveur web Python sur une seule

machine virtuelle dans l'infonuage Openstack. La machine virtuelle doit utiliser l'image INF4410-

Ubuntu-trusty-mini et la flavor INF4410-mini. Elle doit aussi être connectée sur le réseau inf4410-net

pour pouvoir accéder à l'internet.

Il est recommandé de consulter l'exemple suivant:

https://raw.githubusercontent.com/houssemmh/INF4410-TP3/master/hello_world.yaml

Déploiement d'un service Web avec répartition de charge

Vous devez créer un gabarit Heat qui permet de déployer le même service Web, mais cette fois-ci

avec un répartiteur de charge.

Les utilisateurs du service Web devront pouvoir envoyer leurs requêtes à une adresse IP fixe, mais les

différentes requêtes devront pouvoir être traitées de manière transparente par 2 machines virtuelles

différentes.

Un moniteur d'activité doit vérifier le statut des machines à intervalles réguliers. Le moniteur d'activité

envoie un message à intervalles de 12 secondes aux machines pour vérifier leur activité. S'il ne reçoit

pas de réponse dans un délai de 6 secondes, il envoie une seconde requête. S'il ne reçoit pas de

réponse à cette seconde requête dans un autre délai de 6 secondes, il déclare la machine inactive.

Nous fournissons donc avec le travail pratique un gabarit dans lequel devez modifier les sections

identifiées par un commentaire « # À compléter». Vous pouvez aussi vous inspirer de l'exemple

suivant:

https://github.com/openstack/heat-templates/blob/master/hot/autoscaling.yaml
