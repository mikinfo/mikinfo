**Créer un tar en excluant un repertoire**
```
tar --exclude='./cache' -zcvf /var/www/vhosts/xxxxxxxxxx/backup.tgz .
```

**Rechercher une chaîne de caractères dans les fichiers**
```
find /mon/chemin/ -name "*.php" -exec grep -l "textearechercher" {} \;
```

**Backup / Restautation d'une bdd**
```
mysqldump -u user -p databasename > backup.sql (backup)
mysql -u user -p databasename < backup.sql (import)
```

**Trouver et déplacer les fichiers créés depuis plus de 100 jours dans un répertoire donné**
```
find /home/directory/ -maxdepth 1 -mtime +100 -type f -exec ls -l {} \;
find /home/directory/ -maxdepth 1 -mtime +100 -type f -exec mv "{}" /home/directory/archive/ \;
```

**Rsync (copie d'un serveur à l'autre)**
```
rsync -ave ssh login@ftp.cluster023.hosting.ovh.net:/oldir/www /newdir/www
rsync -avzq root@0.0.0.0:/home/directory/* /home/directory/www/ >/dev/null 2>&1
```

**Commandes Symfo**
```
php bin/console cache:clear --env=prod
php bin/console doctrine:schema:update --dump-sql
php bin/console doctrine:schema:update --force
php bin/console debug:container
php bin/console debug:router
php bin/console doctrine:fixtures:load --append
```

**Tuto WSL2**

Configuration de Windows Terminal pour les intéressés
```
https://blog.bobbyallen.me/2019/08/03/an-awesome-linux-terminal-with-microsoft-terminal-and-oh-my-zsh-on-windows-10/
```

Installation LAMP :
```
https://www.benjaminschied.fr/installer-apache-php-mysql-sur-windows-via-wsl/
```

Lorsque vous arrivez sur la partie PHP, suivre le lien suivant :
```
https://www.digitalocean.com/community/tutorials/how-to-run-multiple-php-versions-on-one-server-using-apache-and-php-fpm-on-debian-10-fr
```

Lorsque vous arrivez à la partie BDD, installer phpymadin et pas adminer :
```
https://www.digitalocean.com/community/tutorials/how-to-install-phpmyadmin-from-source-debian-10
```
