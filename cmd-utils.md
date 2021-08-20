<br>**UNIX CMD :**
<br>
<br>**Trouver 20 fichiers lourds d'un dossier**
<br>find .  -type f -printf "%s\t%p\n" | sort -n | tail -20
<br>
<br>**Trouver tous les fichiers supérieur à 100 mo**
<br>find . -type f -size +100M
<br>
<br>**Lister tous les processus d'un utilisateur (nom du site sans extension sous cpanel)**
<br>lsof -u nom_utilisateur
<br>
<br>**Lister les fichiers php qui contiennent un des 3 mot clefs**
<br>grep --include "*.php" -rlE 'viagra|pharma|hacked' .
<br>
<br>**trouver tous les .htaccess dans /var/www**
<br>find /var/www -name ".htaccess"
<br>
<br>**liste les fichiers dans www par date de dernière modification**
<br>find /www -type f -printf '%TY-%Tm-%Td %TT %p\n' | sort -r
<br>
<br>**on peut être plus précis en affichant les fichiers modifiés dans le x (ici 50) dernières minutes**
<br>find /target_directory -type f -mmin -50
<br>
<br>**ou les 24 dernières heures**
<br>find /target_directory -type f -mtime -24
<br>
<br>**on peut enfin choisir une intervalle (entre hier et avant-hier)**
<br>find /target_directory -type f -mtime -48 ! -mtime -24
<br>
<br>**last but not least, déplacer les fichiers qui ont plus de 24h (ou modifié il y a plus de 24h)**
<br>find /target_directory -type f -mtime -24
<br>
<br>**Montre la charge CPU (-u : affiche les processus d'un utilisateur)**
<br>top -u nom_utilisateur
<br>
<br>
<br>**Affiche l'état des processus en cours.**
<br>-ax tous les processus (BSD)
<br>-u informations complètes (BSD)
<br>-e tous les processus (SysV)
<br>-f informations complètes (SysV)
<br>-w lignes larges.
<br>
<br>ps -aux   (BSD)
<br>ps -ef    (SysV)
<br>
<br>**Compresser**
<br>tar -czvf monArchive.tar.gz monRepertoire/
<br>
<br>**Décompresse**
<br>tar -xzvf monArchive.tar.gz
<br>Renommer rapidement un fichier:
<br>cp /home/foo/realllylongname.cpp{,-old}
<br>OU plusieurs
<br>rename

<br>Example:

<br>$ ls
<br>this_has_text_to_find_1.txt
<br>this_has_text_to_find_2.txt
<br>this_has_text_to_find_3.txt
<br>this_has_text_to_find_4.txt
<br>
<br>$ rename 's/text_to_find/been_renamed/' *.txt
<br>$ ls
<br>this_has_been_renamed_1.txt
<br>this_has_been_renamed_2.txt
<br>this_has_been_renamed_3.txt
<br>this_has_been_renamed_4.txt

