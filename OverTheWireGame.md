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
bandit0@bandit.labs.overthewire.org 's  password : ****

--bash
# OverTheWireGame
## Niveau 1
Pour se passer au niveau suivant du jeux :
On doit découvrir d'abord les listes des fichiers dans le répertoire /home/ afin de faciliter le jeu par la commande ls.
Puis on doit connaître les listes des fichiers dans le répertoire bandit0 par la commande classique ls, et on a vue un fichier "readme" qui contient le mot de passe selon le sujet
Et après j'ai utilisé la commande "cat" pour afficher le contenu du fichier "readme"; et j'ai quitté bandit0 pour passer à bandit1 ensuite j'ai nouvelle fois reconnecter pour rentrer à bandit1 en utilisant la SSH et le mot de passe ci-dessus qui se trouve dans le fichier "readme" dans le répertoire de bandit0.

SSH USERNAME@HOST - PORT
--bash

bandit0@bandit:~$ ls /home/
bandit0@bandit:~$ ls 
bandit0@bandit:~$ cat readme

--bash
# OverTheWireGame
## Niveau 2
Pour réussir le niveau 2 :
On utilise la commande ls pour afficher le contenu du répertoire de "bandit 2".
Puis on découvre que le nom du fichier est en forme des caractères speciaux "-" pour cette niveau il est en forme de tiré haut "-". Pour afficher les contenu du fichier, on doit utiliser la commande "cat" avec des caractères "./" et le nom du fichier "-".
"./" designe que je pars de la répertoire où je situe pour aller dans le fichier que j'ai designé après "-".
Et après j'ai utilisé la commande "cat" pour afficher le contenu du fichier "-"; et j'ai quitté bandit1 pour passer à bandit2 ensuite j'ai nouvelle fois reconnecter pour rentrer à bandit1 en utilisant la SSH et le mot de passe ci-dessus qui se trouve dans le fichier "-" dans le répertoire de bandit1.

SSH USERNAME@HOST - PORT
--bash

bandit1@bandit:~$ cat ./-

--bash
# OverTheWireGame
## Niveau 3
Pour passer au niveau 3 :
On peut utiliser la commande ls pour affichier le contenu dans le répertoire "bandit2", une fois qu'on a trouvé le contenu de ce répertoire, il faut qu'on affiche le contenu de ce fichier "spaces in this filename" afin de trouver le code.
Pour accèder au fichier avec des espaces, on doit utiliser un antislash " \ " après chaque mots du fichier sauf au dernier mot du fichier qui n'a pas besoin car un antislash est un séparateur qui remplace l'espace sur le clavier afin de mieux différencier le nom du fichier; et puis on trouve le mot de passe caché pour passer au niveau 3 de bandit.
Et après j'ai utilisé la commande "cat" pour afficher le contenu du fichier "spaces in this filename"; et j'ai quitté bandit2 pour passer à bandit3 ensuite j'ai nouvelle fois reconnecter pour rentrer à bandit3 en utilisant la SSH et le mot de passe ci-dessus qui se trouve dans le fichier "spaces in this filename" dans le répertoire de bandit2.

SSH USERNAME@HOST - PORT
--bash
bandit2@bandit:~$ ls

bandit2@bandit:~$ cat spaces\ in\ this\ filename

--bash
