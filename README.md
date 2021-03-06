Simple sales charts
========


Setup
--------

###### Requirements

The project is a Symfony 4 app built on Ubuntu 18.04 with default installations but any compatible setup should do:

```
PHP 7.2
Nginx 1.14.0 
Mysql 5.7.26
Composer 1.8.6
Node 12.4.0
Yarn 1.16.0
```


###### clone the repository 
```git clone https://github.com/frepper/sales-test.git```

###### move into the project folder 
```cd sales-test```

###### Install dependencies
```composer install```

###### create the database 
```bin/console doctrine:database:create```

###### run migrations 
```bin/console doctrine:migration:migrate```

###### And run the command to import the initial Flinders data
```bin/console flinders:data:setup```

Usage
--------

Once up and running you can find the api swagger docs at: ```http://localhost/api```

The backend call for reporting is: ```http://localhost/products/monthly```

The frontend will be reachable at: ```http://localhost/reports/sales```

Tests can be run with build in phpunit: ```./bin/phpunit```

Front and backend calls are both in the same project for sake of ease but the two are totally independant and data for the reports is loaded through ajax

Screen shot
--------

![screen shot](https://raw.githubusercontent.com/frepper/sales-test/master/data/ScreenshotSalesreports.png)
