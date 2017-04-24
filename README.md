# Hibernate OGM Redis

*Version: 5.1.0.Final - 01-03-2017*

## Description

This project integrates [Hibernate OGM](http://hibernate.org/ogm/) with [Redis](https://redis.io/).	

For running the tests in the _redis_ module an installed Redis server is required. Specify its host name by
setting the environment variable `REDIS_HOSTNAME` prior to running the test suite:

    export REDIS_HOSTNAME=redis-machine

If this variable is not set, the _redis_ module still will be compiled and packaged but the tests will be skipped.
If needed, the port to connect to can be configured through the environment variable `REDIS_PORT`.

Tests with the _redis_ module can be started using a Makefile. The Makefile takes care of downloading and compiling
a recent Redis version, starts a single Redis Standalone and four Redis Cluster nodes and can start the tests.

     make test # Make me happy and run tests against Redis Standalone and Redis Cluster
     make test-standalone
     make test-cluster

Commands to spin up/shut down the Redis instances:

    make start
    make stop

## License

This software and its documentation are distributed under the terms of the
FSF Lesser Gnu Public License (see license.txt).
