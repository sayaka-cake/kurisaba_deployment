# Kurisaba Deployment

:wrench: Please note that local deployment has been tested only on Mac M1 at the moment. 

### Requirements

- docker
- docker-compose
- mysql (could be PosgreSQL, but not tested)

### Preparation

```
# cloning repo
$ git clone https://github.com/sayaka-cake/kurisaba_deployment.git
$ cd kurisaba_deployment

# cloning slightly modified kurisaba repo
$ git clone https://github.com/sayaka-cake/kurisaba.git

# building and deploying containers
$ docker-compose up --build --remove-orphans --force-recreate -d

# import DB file to MySQL
# if you don't have it yet, pls contact the author of repo
# if this command asks any password, just type in `password`
# you can import any available `.sql` file, but it's the most recent file ATM
$ mysql -P 3306 --protocol=tcp -u root -p ku_db < db_2021-10-11+15_34_35-UTC.sql
```

Now you can go to `localhost` in your browser. It will load slow (at least the first time), so be ready.


