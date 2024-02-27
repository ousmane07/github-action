
# GITHUB-ACTION
On a créé un projet SpringBoot nommé github-action 
A la racine du projet on créé un dossier .github. Ce dernier contiendra un dossier nommé workflows qui aura lui aussi en son sein un fichier nommé build.yaml
Vous verrez le contenu de ce fichier dans la capture suivante:

![Capture 1](https://github.com/ousmane07/github-action/blob/master/captures/1.png?raw=true)

Dans le fichier pom.xml, on ajoute le plugin for github action
Dans le plugin, il faut renseigner votre username de votre Docker hub, pour ce faire vous pouvez allez sur hub.docker.com et vous vous connectez, et en haut à droite on clique sur l’initial de notre nom pour récupérer le username

![Capture 2](https://github.com/ousmane07/github-action/blob/master/captures/2.png?raw=true)


Dans la partie properties on ajoute les 2 variables «  docker.user et docker.tocken 

![Capture 3](https://github.com/ousmane07/github-action/blob/master/captures/3.png?raw=true)

Dans la balise build, on ajoute une balise finalname

![Capture 5](https://github.com/ousmane07/github-action/blob/master/captures/5.png?raw=true)

Sur docker hub on génère un token
On clique sur l’initial, my account, à gauche security, new Access Token
Ce Token doit etre copier et stocker quelque part

![Capture 6](https://github.com/ousmane07/github-action/blob/master/captures/6.png?raw=true)

Aller sur github, cliquer sur settings de mon repo, à gauche, secrets and variables, new repo secret 
Name = DOCKER_TOKEN
Secret* = on colle le token 
pui on clique sur ADD SECRET

![Capture 7](https://github.com/ousmane07/github-action/blob/master/captures/7.png?raw=true)

On fait pareil pour ajouter une 2ème variable 
Name = DOCKER_USER
Secret* = le username de docker hub
Ces variables sont utilésées lors de l’execution d’un build

![Capture 8](https://github.com/ousmane07/github-action/blob/master/captures/8.png?raw=true)

On crée une branche nommé ci-cd et on bascule sur cette branche

![Capture 9](https://github.com/ousmane07/github-action/blob/master/captures/9.png?raw=true)

Dans com.groupeisi.demo.web, on ajoute un controller HelloController pour avoir un message

![Capture 10](https://github.com/ousmane07/github-action/blob/master/captures/10.png?raw=true)

Sur github on crée une pull request en cliquant sur l'onglet pull request puis sur new pull request

![Capture 11](https://github.com/ousmane07/github-action/blob/master/captures/11.png?raw=true)

Puis on clique sur l'onglet Action pour lancer le build
On voit que tout est en vert donc ça prouve que ça marche


![Capture 12](https://github.com/ousmane07/github-action/blob/master/captures/12.png?raw=true)

On part sur docker, sur repositories, on voit que le push y est donc tout est OK

![Capture 13](https://github.com/ousmane07/github-action/blob/master/captures/13.png?raw=true)
















