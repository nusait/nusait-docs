##Deploy to the server

### Set up Project Structure
1. Pull down git repo to ```~/www```
2. Go to ```~/html```
3. Make Symbolic Link ```ln -s ../www/projectname/public ./projectname``` (need sudo)
4. Go back to ```~/www/projectname```
5. Go to ```app```
6. Make storage all accessible ```chmod 777 -R storage```

### Set up Server Settings
7. Go to ```~/html/projectname/public```
8. Create the right .htaccess file
9. Create ```database.php``` from ```database-example.php``` in ```app/config```
10. Create ```ldap.php``` from ```ldap-example.php```
(if there isn't one, create ldap.php like so...)

```php
<?php
return array(
  'rdn' => 'your rdn string',
  'password' => 'your password',
);
```
### Load Dependencies
11. ```composer install``` (!!!)
12. run migration and seed