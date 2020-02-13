# MarvelAppInstructions
Instructions concernant l'application Marvel a créer.


# Création PWA Marvel


Pour prendre en mains React nous allons créer une petite application qui présentera nos supers héros préférés.

Le but de l’exercice est de pratiquer React et d’être à l’aise avec la creation de composant, ainsi que la manipulation de donnée retourné par une API.

Cet exercice a pour but de vous faire voir les notions suivantes:

Créer un formulaire controlé (les champs sont relié a la state)
Validateur de formulaires (Vérifier les données entré dans le formulaire)
Créer une application multi-pages avec React-Router
Créer un système de Routes protégés (partie accessible uniquement aux personnes connecté)
Récupérer les paramètres d’une routes (permet de faire un appel API avec l’id d’un personnage par exemple)
Consommé une API, garder certaines informations disponible en hors ligne.
Mise en place d’un système de thème.

Nous avons travailler jusqu’a présent sur une single page App, notre app ne gérer pas le multi-pages, Nous utiliserons React-Routeur pour cela, avant de commencer l’exercice, créer un routeur avec deux pages,  une page login et une page characters. Vous afficherez ce que vous voudrez sur ces pages dans un premier temps.

Les liens de votre routeurs devront être « / » pour le login et « /characters » pour la page characters 

Mettez également un système de redirection si l’utilisateur tape une adresse inexistante.

## I) Formulaire de Connexion

La première étape consiste a créer une page de connexion, dans lequel on aura un formulaire qui permettra aux utilisateur de se connecter.

Recréer la page login (login.png) dans le dossier assets (avec un meilleur design évidemment).

Vous devrez créer plusieurs composants pour cette pages, un composant logo, qui affichera le logo Marvel, un composant loginForm (Que vous pouvez découper en plusieurs composant), qui gérera le formulaire de connexion.

Petite Astuce : Créer les composant directement dans le fichier login puis découper le en plusieurs composant lorsque le tout fonctionne, je vous conseil de commencer comme sa si vous ne vous sentez pas encore à l’aise avec la creation de composant.


Le formulaire doit être un formulaire controlé, c’est a dire que les elements du formulaire (un champ username et password) doivent être géré par la state du composant. (Et non par le biais d’un formulaire HTML classique, via les events).

Le formulaire doit aller récupérer un token de connection à cette adresse:

https://easy-login-api.herokuapp.com/users/login

Il s’agit d’une requête POST qui nécessite un champ username et un champ password

Pas besoin de créer un utilisateur cette API renvoi un token de connection lorsque les deux champs ci dessus sont envoyés.

Il faudra ensuite stocké le token dans le localStorage, puis redirigé l’utilisateur vers la page characters


## II ) Page characters

Vous consommerez l’API Marvel pour afficher une liste des personnages Marvel, vous devez gérer la pagination (faire des requêtes supplémentaire pour avoir la suite de la liste), je vous laisse le choix entre une pagination classique (page 1 - 2 - 3 etc.) ou une pagination infini (chargement de la suite en fin de liste)

Concernant le design inspirez vous du fichier characters dans le dossier assets.

À la selection d’un personnage, on est redirigé vers la page details, qui donnera plus d’informations sur le personnage en questions.

## III ) Page details

Creer une page details , l’ajouter au routeur.

L’adresse de votre page doit être « /characters/:id » 

Le :id signifie que l’info passé a l’url sera un paramètre récupérable ( je vous laisse chercher dans la doc)

Le but de l’exercice est de récupérer le paramètre et de faire une requête API a marvel pour récupérer les informations concernant le personnage.
 


