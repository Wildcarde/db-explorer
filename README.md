# mysql-explorer

This is a small docker based shim for bulk importing sql backup files and giving you a quick web frontend to talk to for browsing the imported data.  Initially I expected this to be more complicated but both the mariadb and postgres stock images have the capacity to import sql and sql.gz files out of the box when wired up right.

## Structure

This system is built from multiple containers handling mariadb, postgres, and the presentation layer (adminer in this case). 

## Environment Variables

### SQL_PW

*default* 'test'; can be used to set the password used for the mysql and postgres databases on startup.

### MYSQLDIR

*default* './data/mysql'
The location data is loaded from for the mysql database, all `.sql` and `.sql.gz` files will be loaded from this folder location.

### PSQLDIR

*default* './data/psql'
The location data is loaded from for the postgresql database, all `.sql` and `.sql.gz` files will be loaded from this folder location.

### ADMINERPORT

*default* '8080'
If you'd like adminer to live somewhere other than port 8080 on the localhost change this to a different port.
