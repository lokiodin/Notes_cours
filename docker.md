# Vagrant Command

Initialiser un VagrantFile dans le dossier courant : `vagrant init`

Lancer le container `vagrant up`, à faire dans le dossier avec le VagrantFile

SSH dans le l'image lancé par `vagrant up` : `vagrant ssh`
	--> à faire dans le dossier du VagrantFile

# Docker Command

Help de docker
`docker help`
`docker container help`

Voir les container en cours d'execution
`docker container ls`
`docker container ps`

Voir les container qui ont été executés et leur nom de container
`docker container ls -a`
`docker container ps -a`

Lance un container hello-world
`docker run <nom_du_container>`

Lancer un container mais le supprimer dès la fin du container
`docker container run --rm <nom_du_container>`


On peut lancer des commande (help à `docker container run --help`) :
`docker container run --rm -it alpine sh` : ici, docker lance le container alpine avec les option i et t pour un tty interactif et lance la commande sh dans le container


Afficher des infos detaillées d'un container
`docker container inspect <nom_du_container>`

Avoir les logs du container
`docker container logs <nom_du_container>`

Supprimer un/des container
`docker container rm <nom_du_container>`

Supprimer TOUS les container stoppé
`docker container prune`

Pull une image d'un repo docker
`docker image pull <nom_de_image>`       ex: `docker image pull alpine`


`docker image build -t <nom_du_prog>`
ex: 
```
echo " FROM scratch
COPY welcome /welcome

CMD ["/welcome"]" > /lab/exo1/Dockerfile.debian


docker image build -t "welcome:c_dynamic"
```