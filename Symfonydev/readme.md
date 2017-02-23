# Symfony dev dockerfile

## instructions
  Caution: use this container for demo purpose only.
  Run the container, mount the volume and put your symfony file into it
  
  This is the defaults database parameters you need in your parameters.yml
  ```yml
     database_host: localhost
    database_port: ~
    database_name: symfony
    database_user: root
    database_password: ~
  ```
  
  After, launch this multiples exec in container
  ```sh
$ service mysql start
$ mysql -e "CREATE DATABASE symfony"
$ chmod a+x -R .
$ composer update
$ php bin/console doctrine:schema:create
$ php bin/console server:run 0.0.0.0:8000
```
