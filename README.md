# xpsql
xpsql is a simple psql wrapper to run queries asynchronously on multiple databases.

## Install
```
$ git clone https://github.com/gma2th/xpsql.git
$ export PATH=$PATH:xpsql
```

## Help
```
$ xpsql --help
xpsql is a simple psql wrapper to run queries asynchronously on multiple databases.

Usage:
  psql [OPTION]... [DBNAMES]

Options:
  -c, --command=COMMAND     execute command, then exit
  -f, --file=FILENAME       execute commands from file, then exit
  -h, --help                show this help, then exit
  -m, --max-line=MAX_LINE   max line to display, print 25, 0 print all
  -s, --services=SERVICES   database services
  -U, --username=USERNAME   database user name
```
## Description:
Command, file and username are unique
Dbnames and services can be multiple
Services are defined in `~/.pg_service.conf`
See https://www.postgresql.org/docs/current/libpq-pgservice.html

## Example
```
$ xsql f $my_query_file -s $my_dbservice_1 -s $my_dbservice_2 $my_db_uri_1 $my_db_uri_2
```
