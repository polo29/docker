# FROM permet de d�finir depuis quelle base votre image ve �tre cr��e
FROM debian
#MAINTAINER permet de d�finir l'auteur de l'image et s'�crit de la mani�re suivante Nom <email>
MAINTAINER Marc ESCARMANT
# RUN permet de lancer une commande, mais aura aussi pour effet de cr�er une image interm�diaire.
RUN apt-get update
RUN apt-get -y install wget
#RUN apt-get -y install nginx
# ADD permet de copier un fichier depuis la machine h�te ou depuis une URL
#~ADD http://www.tito.com/script.sh ou /chemin/script.sh ou script.sh  /chemin/destination
ADD script.sh /usr/bin/script.sh
RUN chmod +x /usr/bin/script.sh
# EXPOSE permet d'exposer un port du container vers l'ext�rieur
EXPOSE 80
# ENTRYPOINT permet d'ajouter une commande qui sera ex�cut�e par d�faut, et ce, 
ENTRYPOINT ["script.sh"]
# CMD d�termine la commande qui sera ex�cut�e lorsque le container d�marrera
CMD ["bash"]
# m�me si on choisit d'ex�cuter une commande diff�rente de la commande standard
# WORKDIR permet de d�finir le dossier de travail pour toutes les autres commandes 
#(par exemple RUN, CMD, ENTRYPOINT et ADD)
# ENV permet de d�finir des variables d'environnements qui pourront ensuite �tre modifi�es gr�ce 
# au param�tre de la commande run --env <key>=<value>.
# VOLUMES permet de cr�er un point de montage qui permettra de persister les donn�es. 
# On pourra alors choisir de monter ce volume dans un dossier sp�cifique en utilisant la commande `run -v :
VOLUME /volume/data
