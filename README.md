# docker_for_mvc_framework
Simple docker configuration for PHP-MVC framework like Laravel.
The **tmp** folder under the **docker_for_mvc_framework** must be available for writing to all. For example `sudo chmod -R a+w tmp`

## Updates

* **2022-03-23**

  - the **tmp** folder under the **docker_for_mvc_framework** must be available for writing to all. For example `sudo chmod -R a+w tmp`

* **2022-03-04**

  - map tmp for easy access to **cachegrind** files

* **2022-03-04**

  - update the xdebug.ini for profiling. In some cases use parameters `XDEBUG_PROFILE` and `XDEBUG_TRIGGER`. For example for `GET` parameters `?XDEBUG_PROFILE=1&XDEBUG_TRIGGER=1`
  - sample configuration for **VSCode** for **Listen for Xdebug** section: 
```
"configurations": [
        {
            "name": "Listen for Xdebug",
            "type": "php",
            "request": "launch",
            "port": 9003,
            "hostname": "0.0.0.0",
            "pathMappings": {
                "/app": "${workspaceFolder}/app"
            },
            "log": true
        },
        ...
        ...
```

* **2022-03-03**

  - added xdebug.ini and necessery config for debugging

