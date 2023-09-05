# DNS Windows

**Étape 1 : Installation du rôle DNS**                            
- On Ouvre le Gestionnaire de serveur sur Windows Server.                                  
- On clique sur "Gérer" dans le coin supérieur droit, puis on sélectionne "Ajouter des rôles et fonctionnalités".                                            
- On Coche la case "Serveur DNS" dans la liste des rôles disponibles. Et On suit les étapes de l'Assistant pour terminer l'installation                                   

**Étape 2 : Configuration de la zone DNS**                                                
- Ouvrir le Gestionnaire DNS.                                       
-  Créer une nouvelle zone primaire "wilders.lan".                                              
![wilders lan](https://github.com/omaymaaboumoussa/DNS/assets/137881447/80acbb68-ade9-444e-bc3e-efcf2ea3ca66)

  
![1](https://github.com/omaymaaboumoussa/DNS/assets/137881447/d7e6c7fa-1ced-457f-8031-5759e219106c)

  
-  Ajouter un Hote A pour le serveur et la machine avec une réservation IP fixe.             

  ![55](https://github.com/omaymaaboumoussa/DNS/assets/137881447/bcf143ec-c5e7-4beb-ad84-e2224b6c7294)

-  Ajouter un enregistrement CNAME pour le serveur ("dns.wilders.lan").

  ![wilders dns](https://github.com/omaymaaboumoussa/DNS/assets/137881447/b82d8a41-5e46-4567-8ae9-b2ead7b303b5)

  ![4](https://github.com/omaymaaboumoussa/DNS/assets/137881447/7de3bc10-de5f-45fa-949d-a178c3016ed8)
 Dans la zone inversé on trouve:
 
![5](https://github.com/omaymaaboumoussa/DNS/assets/137881447/43ffadd6-a184-488c-937a-ace248d7b8c5)


**Étape 4 : Test de la résolution**                                  
                 
- Pour tester la résolution de noms, On ouvre une invite de commandes sur le serveur et la machine cliente, et on utilise la commande "nslookup".                                  
 Pour résoudre le nom du serveur : nslookup wilders.lan                                               
 Pour résoudre le CNAME : nslookup dns.wilders.lan                                            

**Étape 5 : Test de la résolution inverse**                                      

- Sur le serveur, On utilise nslookup avec l'adresse IP du serveur et de la machine fixe.


