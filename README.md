docker-postgresql
=================

PostgreSQL for Docker. The data directory is set to `/data` so you can use a data only volume.

    $ docker run -name postgresql-data -v /data ubuntu /bin/bash
    $ docker run -d -p 5432:5432 -v /HOST/DATA:/data -v /HOST/XLOG:/xlog -e POSTGRESQL_USER=docker -e POSTGRESQL_PASS=docker -e POSTGRESQL_DB=docker asherwin/postgresql
    da809981545f
    $ psql -h localhost -U docker docker
    Password for user docker:
    psql
    Type "help" for help.

    docker=#

(Example assumes PostgreSQL client is installed on Docker host.)

