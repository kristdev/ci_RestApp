
# Ci Rest App (Codeigniter Restfull Application) #

Ci Rest App est la toute première application Rest PHP basée sous codeigniter visant à tutorer la communauté Ci pour des implémentations de REST. Par soucis de modularité, elle sera construite autour de l'archtecture HMVC, et tournera sous mysql dans un premier temps, une autre version future tournera sous mongodb. 

Egalement, dans le futur, des versions améliorées seront basées sous websocket, toujours dans le but d'améliorer des communications synchrones entre un serveur et un client.

## Description du projet ##
*Le projet est assez simple:*


- Des utilisateurs d'un système écrivent un ou plusieurs articles,
- Un article a un ou plusieurs commentaires,
- Un commentaire est fait par un seul utilisateur, et plusieurs peuvent commenter.

*Voici le shémas de notre système, assez simple. Il y'a donc 3 tables principales,*

- **utilisateurs**(id[int 4], name[varchar 120], username[varchar 25], email[varchar 55], password[varchar 255])
- **articles**(id[int 4], title[varchar 120], content[longtext])
- **commentaires**(id[int 4], content[varchar 160])

*Ce que nous recherchons comme fonctionalités, c'est:*

1. Lire sur une page les intro des différents articles, avec en mention le username de l'auteur et le nombre de commentaires associé à l'article.
2. Lire sur une autre page l'article au complet avec les différents commentaires, la mention étant les usernames des utilisateurs ayant commentés.
3. Dans une fenêtre modale, on devra avoir les informations de l'utilisateur après click sur son username(Infos de base, nombre d'articles écrit, nombre de participations ou commentaires, les titres d'articles écrits, et les titres d'articles commentés).
4. Dans une page, créer un compte utilisateur et renvoyer le résultat
5. Dans une page, se connecter et être redirigé vers un espace perso
6. Le dashboard de cet espace a des stats de posts d'articles et commentaires, mais également des suivis, c'est à dire des commentaires recupérés sur les articles postés.
	
Dans un premier temps, voilà ce que nous recherchons comme fonctionalités.

## Organisation du projet  ##
L'application à notre étude connaîtra un dossier client, entirement rédigé en html+js, un dossier pour notre api, supporté par codeigniter, et un dossier administrateur rédigé également en html+js.

**Les clients et les administrateurs communiqueront avec notre api par requetes http.**

**NB:** *Nous utiliserons quelques plugins, librairies et frameworks, PHP et js, parmi lesquels,*

- HMVC Codeigniter
- Angularjs
- Bootstrap
- font-awesome


1. [Data analysyis](./dataanalysis.md "Data analysis")
2. [Data generating ](./datagenerating.md "Data generating")