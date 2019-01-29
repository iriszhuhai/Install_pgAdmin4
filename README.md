# Install_pgAdmin4_on_Ubuntu_16.04/18.04

I tried many ways to install pgAdmin4 on Ubuntu 16.04/18.04, every time I got different errors. Following the below instructions will help successfully install pgAdmin4 Desktop on Ubuntu.
#### Install virtual environment and create pgadmin4 virtual environment

```
$ sudo apt-get install virtualenv python-pip libpq-dev
$ virtualenv pgadmin4
```
#### Activate pgadmin4
```
$ cd ~/pgadmin4
$ source bin/activate
```
#### Download pgadmin4
Note: this link may change in the future, if it can not download the 'whl' file, try to check the link https://ftp.postgresql.org/pub/pgadmin/pgadmin4/ and install the latest version of pgadmin.

```
$ wget https://ftp.postgresql.org/pub/pgadmin/pgadmin4/v1.4/pip/pgadmin4-1.4-py2.py3-none-any.whl
```
#### Install pgadmin4

```
$ pip install  pgadmin4-1.4-py2.py3-none-any.whl -U psycopg2
```
"-U psycopg2" makes sure you install all dependencies and upgrade psycopg2.

#### Config
single-user mode
```
$ echo "SERVER_MODE = False" >> ~/pgAdmin4/lib/python2.7/site-packages/pgadmin4/config_local.py
```
#### Start your pgAdmin
```
$ python lib/python2.7/site-packages/pgadmin4/pgAdmin4.py
```
It returns: 
....
Starting pgAdmin 4. Please navigate to http://localhost:5050 in your browser.

##### Here you will successfully run pgAdmin4. Enjoy!


