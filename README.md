## base_drf_mysql


_If you would like this repo without mysql, please refer to base_drf_


### First build

Note: it is required to run build with option to remove intermediate containers

```sh
> docker-compose build --force-rm
```

On initial docker build the following packages were installed:
- Django==2.2.10
- django-mysql==3.3.0
- djangorestframework==3.10.3
- flake8==3.6.0
- mccabe==0.6.1
- mysqlclient==1.4.6
- pycodestyle==2.4.0
- pyflakes==2.0.0
- pytz==2019.3
- sqlparse==0.3.0



### Note - for Linux users, on file and folder permissions

In your `.bashrc` add following lines
```sh
function guid() {
  export uid=${UID}
  export gid=${GID}
}
```
Run `guid` command from terminal in your project directory before each run
, so you don't have problems with permissions, or configure your `.bashrc
` so this command is run every time on terminal start


### Travis CI

If you don't want to implement Travis Continuous Integration, delete `.travis
.yml` file.


### Flake8

To run tests with flake8 linting support, run
```sh
> docker-compose run --rm app sh -c "python manage.py test && flake8"
```

