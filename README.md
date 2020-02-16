#ISTRUZIONI

1. verificare di avere installato Composer con <code>composer -v</code> 
2. creare il database e assegnare uno user di nome drupal con una password "drupal"
3. cd htdocs
4. cd cartella-del-progetto
5. composer create-project drupal/recommended-project my_site_name_dir
6. composer require drush/drush -vvv (potrebbe metterci molto tempo)
7. drush site:install se questo comando non funziona creare un file drush.bat nella stessa cartella dove si trova drush.phar contenente <code>@echo off</code> <code>php "%~dp0\drush.phar" %*</code>

link https://www.drupal.org/docs/develop/using-composer/using-composer-to-install-drupal-and-manage-dependencies

per installare un modulo usare il comando composer require drupal/<modulename> (per installarne diversi insieme usare composer require drupal/<modulename> drupal/<othermodulename> )
per attivarlo drush en <modulename>

in caso di problemi di memoria usare il comndo php --ini per trovare il percorso del file .ini e settare ; Maximum amount of memory a script may consume (128MB)
; http://php.net/memory-limit
memory_limit=-1

##Dati di accesso
visitare http://localhost/appuntidigitali/web/
User name: admin  User password: ACMJ3okYfc