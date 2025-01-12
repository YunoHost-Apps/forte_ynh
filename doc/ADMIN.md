### Register a new domain and add it to YunoHost

- Your [Forte](https://codeberg.org/fortified/forte/) website requires a dedicated domain, so obtain one and add it using the YunoHost admin panel. **Domains -> Add domain**. As your website uses the full domain and is installed on the root, you can create a subdomain such as mywebsite.domain.tld. Don't forget to update your DNS records if you manage them manually.

### Admin user rights, logs and failed database updates

- **Admin account**: When installation is complete, you must visit your new website and create the first account using the **admin's email address** (the admin is the YunoHost user which was chosen at the beginning of the installation process). You will then be able to create your first channel and have access the **admin pages** for your website.

- **Failing to get admin rights**: If the admin cannot access the admin settings at `https://mywebsite.domain.tld/admin` or you want to grant admin rights to any other registered user on your website, then you have to **manually add 4096** to the ***account_roles*** under ***accounts*** for that user in the **database through software like phpMyAdmin**.

- **Failed Database after Upgrade**: If the database upgrade fails after version upgrade, you can visit the dedicated page, `https://mywebsite.domain.tld/admin/dbsync/`, and check the numbers of failed updates. These updates will have to be ran manually using software such as **phpMyAdmin**.

### Custom configuration

- **Additional settings in .htconfig.php**: If you need to add some additional lines in .htconfig.php (as described on the [Service Classes](https://codeberg.org/fortified/forte/src/branch/release/doc/admin/en/Service_Classes.mc) or [PHPMailer](https://codeberg.org/fortified/forte/src/branch/release/doc/admin/en/SMTP.mc) documentation), please add it in the `/home/yunohost.app/forte/extra_conf.php` file (or `/home/yunohost.app/forte__X/extra_conf.php` if you installed more than one site). Do not touch .htconfig.php as your changes will be wiped when the YunoHost package is upgraded.
