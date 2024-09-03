### Enregistrez un nouveau domaine et ajoutez-le à YunoHost

- Votre site [Forte](https://codeberg.org/fortified/forte/) nécessite un domaine dédié, alors obtenez-en un et ajoutez-le à l'aide du panneau d'administration YunoHost. **Domaines -> Ajouter un domaine**. Votre site utilise un domaine complet et est installé à la racine, vous pouvez donc créer un sous-domaine tel que monsite.domaine.tld. N'oubliez pas de mettre à jour vos enregistrements DNS si vous les gérez manuellement.

### Droits d'utilisateur de l'administrateur, journaux et échec des mises à jour de la base de données

- **Compte administrateur** : lorsque l'installation est terminée, vous devez vous rendre sur la page d'accueil de votre nouveau site et créer le premier compte en utilisant **l'adresse électronique de l' administrateur** (l'administrateur est l'utilisateur YunoHost qui a été choisi au début du processus d'installation). Vous pouvez ensuite créer votre premier canal et accéder à **l'interface d'administration** de votre site.

- **Échec de l'obtention des droits d'administration** : si l'administrateur ne peut pas accéder aux paramètres d'administration sur `https://monsite.domaine.tld/admin`, vous devez **ajouter manuellement 4096** aux ***account_roles*** sous ***accounts*** pour cet utilisateur dans la **base de données** par exemple via **phpMyAdmin**.

- **Pour les logs** : Allez dans **admin->logs** et saisissez le nom du fichier **/var/log/forte/php.log**.

- **Échec de la base de données après la mise à niveau** : Parfois, la mise à niveau de la base de données échoue après la mise à niveau de la version. Allez sur la page dédiée de votre site, `https://monsite.domaine.tld/admin/dbsync/`, et vérifiez les références de mises à jour défaillantes. Ces mises à jour devront être exécutées manuellement, sur **phpMyAdmin**.

### Configuration personnalisée

- **Paramètres additionnels dans .htconfig.php** : Si vous avez besoin d'ajouter des lignes supplémentaires dans .htconfig.php (comme décrit dans la documentation de [Service Classes](https://codeberg.org/streams/streams/src/commit/c75afc9ab4b9ba19628008c14459756edf9c291a/doc/admin/en/Service_Classes.mc) ou de [PHPMailer](https://codeberg.org/streams/streams/src/commit/c75afc9ab4b9ba19628008c14459756edf9c291a/doc/admin/en/SMTP.mc)), veuillez les ajouter dans le fichier `/home/yunohost.app/forte/extra_conf.php` (ou `/home/yunohost.app/forte__X/extra_conf.php` si vous avez installé plusieurs sites). Ne touchez pas à .htconfig.php car vos modifications seront effacées lors de la mise à jour du paquet YunoHost.

