## RDS connection examples for Open Telekom Cloud ##
Below Open Telekom Cloud Relational Database services are currently covered by examples:
- MySQL
- PostgreSQL
- MS SQLServer


## MySQL ##

### Python - examples/MySQL-inserts.py ###
Please refer the [MySQL Connector/Python Developer Guide](https://dev.mysql.com/doc/connector-python/en/) documentation article that describes how to install and configure MySQL Connector/Python, a self-contained Python driver for communicating with MySQL servers, and how to use it to develop database applications. 

Code example is based on [mysql-connector-python/examples/inserts.py](https://github.com/mysql/mysql-connector-python/blob/master/examples/inserts.py), but TABLE creation is modified to increase compatibility

Step by step guide
- Create MySQL database on OTC 
- Create ECS and setup connection with MySQL client using the [User guide](https://docs.otctest.t-systems.com/en-us/rds_dld/index.html)
- Create database test as it's used in the examples
- Have a working Python environment
- Install MySQL Connector/Python as documented in [MySQL Connector/Python Developer Guide](https://dev.mysql.com/doc/connector-python/en/)
- Modify the source code to include connection parameters of your RDS MySQL
 ```
     config = {
        'host': '_host_ip_',
        'port': 8635,
        'database': 'test',
        'user': 'root',
        'password': '_password_',
```        
- Execute the example code from examples/MySQL-inserts.py

Example using MySQL Connector/Python showing:
* dropping and creating a table
* inserting 3 rows using executemany()
* selecting data and showing it

## PostgreSQL ##

### Python - examples/PostgreSQL-usercast.py ###
Please refer the [Psycopg2 Tutorial](https://wiki.postgresql.org/wiki/Psycopg2) documentation article that describes how to install and configure Psycopg2 a PostgreSQL database adapter for the Python programming language, and [how to use it to develop database applications](https://wiki.postgresql.org/wiki/Psycopg2_Tutorial). 

Code example is based on [psycopg2/examples/usercast.py](https://github.com/psycopg/psycopg2/blob/master/examples/usercast.py), but modified to increase compatibility by using standard random library 

Step by step guide
- Create PostgreSQL database on OTC 
- Create ECS and setup connection with PostgreSQL client using the [User guide](https://docs.otctest.t-systems.com/en-us/rds_dld/index.html)
- Create database test as it's used in the examples
- Have a working Python environment
- Install Psycopg2 as documented in [Psycopg2 wiki](https://wiki.postgresql.org/wiki/Psycopg2) more details and installation options at [Psycopg dev documentation](http://initd.org/psycopg/docs/install.html)
- Modify the source code to include connection parameters of your RDS
 ```
## put in DSN your DSN string

DSN = "host='_host_ip_' port=8635 dbname='testdb' user='root' password='secret'"
```        
- Execute the example code from examples/PostgreSQL-usercast.py

Example using Psycopg2 showing:
* dropping and creating a table
* inserting 100 rows
* selecting data and showing it

## MS SQLServer ##

### Python - examples/mssql-inserts.py ###
Please refer the [Pymssql Introduction](http://pymssql.org/en/stable/intro.html) documentation article that describes how to install and configure Pymssql a MS SQLServer database adapter for the Python programming language, and [how to use it to develop database applications](http://pymssql.org/en/stable/pymssql_examples.html). 

Code example is based on [Pymssql examples](http://pymssql.org/en/stable/pymssql_examples.html)

Step by step guide
- Create MS SQLServer database on OTC 
- Create ECS and setup connection with MS SQLServer client using the [User guide](https://docs.otctest.t-systems.com/en-us/rds_dld/index.html)
- Check connectivity tempdb database will be used in the examples
- Have a working Python environment
- Install Pymssql as documented in [Pymssql Installation](http://pymssql.org/en/stable/intro.html#install) more details and installation options at [Pymssql  building and developing](http://pymssql.org/en/stable/building_and_developing.html)
- Set env variables to set connection parameters of your RDS
 ```
export PYMSSQL_TEST_SERVER=_host_ip_:8433
export PYMSSQL_TEST_USERNAME=rdsuser
export PYMSSQL_TEST_PASSWORD=_secret_
```        
- Execute the example code from examples/mssql-inserts.py

Example using Pymssql showing:
* dropping and creating a table
* inserting 3 rows
* selecting data and showing it
