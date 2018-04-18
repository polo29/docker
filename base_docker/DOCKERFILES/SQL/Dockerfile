# FROM permet de définir depuis quelle base votre image ve être créée
FROM debian:latest
#MAINTAINER permet de définir l'auteur de l'image et s'écrit de la manière suivante Nom <email>
MAINTAINER Marc ESCARMANT
# RUN permet de lancer une commande, mais aura aussi pour effet de créer une image intermédiaire.
RUN apt-get update  
RUN apt-get -y install vim
RUN apt-get -y install mariadb-server
# ADD permet de copier un fichier depuis la machine hôte ou depuis une URL
#~ADD http://www.tito.com/script.sh ou /chemin/script.sh ou script.sh  /chemin/destination
ADD marcotest.sh /usr/bin/marcotest.sh
RUN chmod +x /usr/bin/marcotest.sh
# EXPOSE permet d'exposer un port du container vers l'extérieur
EXPOSE 3306 
# ENTRYPOINT permet d'ajouter une commande qui sera exécutée par défaut, et ce, 
#ENTRYPOINT ["marcotest.sh"] #Apres execution ça sort du contener !!!!
# CMD détermine la commande qui sera exécutée lorsque le container démarrera
#CMD ["bash"]
# même si on choisit d'exécuter un #Apres execution ça sort du contener !!!!e commande différente de la commande standard

#VOLUME /volume/data
###

# WORKDIR permet de définir le dossier de travail pour toutes les autres commandes 
#(par exemple RUN, CMD, ENTRYPOINT et ADD)
###


# ENV permet de définir des variables d'environnements qui pourront ensuite être modifiées grâce 
# au paramètre de la commande run --env <key>=<value>.
# VOLUMES permet de créer un point de montage qui permettra de persister les données. 
# On pourra alors choisir de monter ce volume dans un dossier spécifique en utilisant la commande `run -v :
