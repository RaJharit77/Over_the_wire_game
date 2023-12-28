# OverTheWireGame
## Niveau 0
Mais avant je suis connecté sur mon ordinateur virtuelle afin de rassurer la continuation du jeux :
HostName(or IP address) : 192.168.91.131
Login as : rajoharitiana
rajoharitiana@192.168.91.131's password : ******

Pour se connecter, on utilise le commande SSH en suivant le template ci-dessous : 
SSH USERNAME@HOST - PORT
--bash
HostName (or IP address ) : bandit.labs.overthewire.org  - port : 2220
Login as : bandit0
bandit0@bandit.labs.overthewire.org 's  password : bandit0
bandit0@bandit:~$
---
# OverTheWireGame
## Niveau 1
Pour se passer au niveau suivant du jeux :
On doit découvrir d'abord les listes des fichiers dans le répertoire /home/ afin de faciliter le jeu par la commande ls.
Puis on doit connaître les listes des fichiers dans le répertoire bandit0 par la commande classique ls, et on a vue un fichier "readme" qui contient le mot de passe selon le sujet
Et après j'ai utilisé la commande "cat" pour afficher le contenu du fichier "readme"; et j'ai quitté bandit0 pour passer à bandit1 ensuite j'ai nouvelle fois reconnecter pour rentrer à bandit1 en utilisant la SSH et le mot de passe ci-dessus qui se trouve dans le fichier "readme" dans le répertoire de bandit0.
SSH USERNAME@HOST - PORT
--bash
bandit0@bandit:~$ [ls /home/]
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
rajoharitiana@dellg:~$ ssh bandit1@bandit.labs.overthewire.org -p 2220
bandit1@bandit.labs.overthewire.org's password : NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit1@bandit:~$
---
# OverTheWireGame
## Niveau 2
Pour réussir le niveau 2 :
On utilise la commande ls pour afficher le contenu du répertoire de "bandit 2".
Puis on découvre que le nom du fichier est en forme des caractères speciaux "-" pour cette niveau il est en forme de tiré haut "-". Pour afficher les contenu du fichier, on doit utiliser la commande "cat" avec des caractères "./" et le nom du fichier "-".
"./" designe que je pars de la répertoire où je situe pour aller dans le fichier que j'ai designé après "-".
Et après j'ai utilisé la commande "cat" pour afficher le contenu du fichier "-"; et j'ai quitté bandit1 pour passer à bandit2 ensuite j'ai nouvelle fois reconnecter pour rentrer à bandit1 en utilisant la SSH et le mot de passe ci-dessus qui se trouve dans le fichier "-" dans le répertoire de bandit1.
SSH USERNAME@HOST - PORT
--bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
rajoharitiana@dellg:~$ ssh bandit2@bandit.labs.overthewire.org -p 2220
bandit2@bandit.labs.overthewire.org's password: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit2@bandit:~$
---
# OverTheWireGame
## Niveau 3
Pour passer au niveau 3 :
On peut utiliser la commande ls pour affichier le contenu dans le répertoire "bandit2", une fois qu'on a trouvé le contenu de ce répertoire, il faut qu'on affiche le contenu de ce fichier "spaces in this filename" afin de trouver le code.
Pour accèder au fichier avec des espaces, on doit utiliser un antislash " \ " après chaque mots du fichier sauf au dernier mot du fichier qui n'a pas besoin car un antislash est un séparateur qui remplace l'espace sur le clavier afin de mieux différencier le nom du fichier; et puis on trouve le mot de passe caché pour passer au niveau 3 de bandit.
Et après j'ai utilisé la commande "cat" pour afficher le contenu du fichier "spaces in this filename"; et j'ai quitté bandit2 pour passer à bandit3 ensuite j'ai nouvelle fois reconnecter pour rentrer à bandit3 en utilisant la SSH et le mot de passe ci-dessus qui se trouve dans le fichier "spaces in this filename" dans le répertoire de bandit2.
SSH USERNAME@HOST - PORT
--bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit3@bandit:~$
---
[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
