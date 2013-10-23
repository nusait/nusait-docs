## Prepare the first commit
1. ```mkdir projectname && cd $_```
2. ```composer create-project laravel/laravel projectname .```
3. Create database-example.php ```cp app/config/database.php app/config/database-example.php```
4. Create ldap-example.php ```touch app/config/ldap-example.php```

```php
<?php
return [
  'rdn' => 'your rdn string',
  'password' => 'password'
];
```
5. Update [.gitignore](https://github.com/nusait/nusait-docs/blob/master/.gitignore) file
6. Inside ```bootstrap/start.php``` Update local environment value to 'localhost' (or your other dev paths)
7. Set up other environment values if necessary
8. ```composer install```
9. make sure you can see the page in your browser

## Optional Mailing Configs
1. Change ```app/config/mail.php``` ```driver``` value to ```mail```
2. Copy ```mail.php``` to ```app/config/local``` and set up your mail config

## Start Git
1. In the root of your folder ```git init```
2. ```git add . ```
3. ```git status ```
4. ```git commit -m 'initial commit' ```

## Optional NuAuth Package
1. If you are going to use LDAP to authenticate users, include our very own NuAuth Package (package readme).
2. Set up users table
3. Include Package

