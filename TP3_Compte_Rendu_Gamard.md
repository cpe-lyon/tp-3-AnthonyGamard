# Compte rendu TP3
## Exercice 1 : Gestion des utilisateurs et des groupes

### Question 1 
-sudo groupadd (dev/infra)

### Question 2
-sudo useradd (dave/charlie/bob/alice)

### Question 3 
-sudo gpasswd -a (alice/bob) dev 
-sudo gpasswd -a (dave/charlie) infra

### Question 4 
On peut afficher les membres du group infra avec la commande 
-getent group infra

### Question 5 
on utilise les commandes suivantes : 
-sudo chgrp dev /home/(alice/bob)
-sudo chgrp infra /home/(dave/charlie)

### Question6 
on modifie les group primaire avec les commandes suivantes :
-sudo usermod -g dev (alice/bob)
-sudo usermod -g infra (charlie/dave)

### Question 7 
pour créer les répertoire on utilise la commande -mkdir (dev/infra)
pour changer les droits on utilise -sudo chmod g=wr (dev/infra)

### Question 8
-chmod u=rwx

### Question 9 
On ne peut pas se connecter le compte de alice n'a pas été paramétré.

### Question 10
Pour commencer on a attribué un passwd a alice avec la commande -sudo passwd alice
et ensuite on a activé son compte -sudo passwd --unlock alice la connexion est possible. 

### Question 11
On peut obtenir les informations avec la commande -id alice

### Question 12 
la commande est -id 1003

### Question 13
l'id du groupe dev est 1008.

### Question 14 
c'est le groupe dev 

### Question 15 
-sudo gpasswd --delete charlie infra

### Question 16 
-sudo usermod -e 2021-06-01 dave
-sudo chage -M 90 dave
-sudo passwd -n 5 dave
-sudo chage -W 14 dave
-sudo usermod -f 30 dave

### Question 17 
grep root /etc/passwd : L'interpréteur de commande de root est bash 

### Question 18 
L'utilisateur nobody est le nom d'un compte à qui appartient aucun groupe ou fichier et dont tous ses droits son contraires au autre utilisateur.

## Exercice 2  

### Question 1
Pour créer le dossier on fait la commande : mkdir /test
on peut mettre des lignes de texte en l'ouvrant avec nano ou vim 

### Question 2 
Pour retirer les droit on fait la commande suivante : chmod 000 test
Avec le root le fichier est quand même modifiable car root à toujours les droit.

### Question 3 
On redonne les droit chmod 777 test
On peut de nouveau modifier le fichier sans les droits root.

### Question 4 
Le fichier est modifiable avec ou sans root car on a redonné les droit sur la question d'avant.

### Question 5 
Si on retire les droits il est impossible de lister ou d'afficher le contenu du fichier.
on test avec la commande ls test 

### Question 6 
mkdir sstest
touch nouveau
chmod u-w sstest
chmod u-w nouveau

Si les droits d'écriture son retiré il est impossible d'éditer le fichier.

### Question 7 
Pour créer le dossier : 
mkdir test
chmod -x test

Créer le fichier : 
touch test/file

Supprimer le fichier : 
rm -rf test/file

Modifier : 
touch test/file 

Moove : 
cd test 

On a pu voir que les droits d'exécution bloque toutes les actions sur un directory.

### Question 8 
Pour modifier ou supprimer un fichier les droits dépendent du fichier lui même et non pas du répertoire courant du fichier.

Si les droits sont retirer directement sur le répertoire il sera impossible d'ouvrir ou de modifier le fichier.

### Question 9 
On rétablit les droits 
on peut regarder les droits avec ls -l  

### Question 10 
On retire les droits au autres utilisateur 
umask 077
touch essaie

### Question 11 
umask 022
mkdir dossier
touch file

### Question 12 
umask 047
umask -S

### Question 13


