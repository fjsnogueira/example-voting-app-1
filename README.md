Instavote
=========

Getting started
---------------

Download [Docker for Mac or Windows](https://www.docker.com).

![open in vs code](https://cloud.githubusercontent.com/assets/1487073/18072204/1a42e498-6e11-11e6-889f-3710890c6ac2.png)

![open in vs code2](github-mac:https//github.com/Microsoft/open-from-github.git)

``` bash
git clone ...
npm install
```

Run this command:

``` bash
    $ docker-compose up
```

The app will be running at [http://localhost:5000](http://localhost:5000), and the results will be at [http://localhost:5001](http://localhost:5001).

Architecture
-----

![Architecture diagram](architecture.png)

* A Python webapp which lets you vote between two options
* A Redis queue which collects new votes
* A .NET worker which consumes votes and stores them in…
* A Postgres database backed by a Docker volume
* A Node.js webapp which shows the results of the voting in real time

