#TeamSpeak Server On Dotcloud
C'est un portage du serveur de VoIP Teamspeak pour dotCloud. Ce serveur de VoIP est accompagné d'une interface web d'administration.
Lors du déploiement, le serveur est fonctionnel instantanément.

##Comment ça marche ?
Il récupère les packages :
- Pour le serveur TeamSpeak sur le site officiel
- Pour l'interface Web sur un mirror
Et configure le serveur et l'interface Web selon les contraintes imposées par dotCloud via des scripts. 

##Comment l'utiliser ?
- Faites un clone de ce Git
- Ouvrez le fichier `postinstall` et ajoutez votre mot de passe dans la ligne
```SERVERADMIN_PASSWORD="Enter_Your_Password_Here"```
- Et faites un dotCloud Push:
```dotcloud push applicationname```
A la fin de ce push, les adresses (et le port) du serveur TeamSpeak et de l'interface Web seront affichées.

##Comment administrer le serveur Teamspeak ?
###Soit classiquement par le client TeamSpeak grâce à la clé de privilège.
A la première connexion au serveur avec un client TeamSpeak, une clé de privilège vous sera demandée. Vous pouvez la récupérer en exécutant cette commande:
```dotcloud run applicationname.ts3 cat privilege_key```
###Soit par l'interface Web d'administration
Pour accéder a l'interface Web d'administration, veuillez saisir le lien qui vous a été fourni a la fin du Push.
**Le mot de passe superadmin est celui que vous avez mis dans le fichier `postinstall`**

##Remerciements
- Psychokiller pour son interface Web (http://interface.ts-rent.de)
- Bob_51_ pour la traduction du ReadMe