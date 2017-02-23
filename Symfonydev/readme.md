# Symfony dev dockerfile

## instructions
  Caution: use this container for demo purpose only.
  Run the container, mount the volume and put your symfony file into it
  
  After, launch this multiples exec in container
  ```sh
$ service mysql start
$ mysql -e "CREATE DATABASE symfony"
$ chmod a+x -R .
$ composer update
$ php bin/console server:run 0.0.0.0:8000
```
