Instavote
=========

Getting started
---------------

Download [Docker for Mac or Windows](https://www.docker.com).

![Open in VS Code](https://cloud.githubusercontent.com/assets/1487073/18072108/6988f606-6e10-11e6-87aa-968d3d1f19dd.png =100x20)

Run in this directory:

    $ docker-compose up

The app will be running at [http://localhost:5000](http://localhost:5000), and the results will be at [http://localhost:5001](http://localhost:5001).

Architecture
-----

![Architecture diagram](architecture.png)

* A Python webapp which lets you vote between two options
* A Redis queue which collects new votes
* A .NET worker which consumes votes and stores them in…
* A Postgres database backed by a Docker volume
* A Node.js webapp which shows the results of the voting in real time

