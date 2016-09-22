# zeppelin

A `debian:jessie` based Spark and [Zeppelin](http://zeppelin.incubator.apache.org) Docker container.

This image is large and opinionated. It contains:

- [Spark 1.6.1](http://spark.apache.org/docs/1.6.1) and [Hadoop 2.6.3](http://hadoop.apache.org/docs/r2.6.3)
- [PySpark](http://spark.apache.org/docs/1.6.1/api/python) support with [Python 3.4](https://docs.python.org/3.4), [NumPy](http://www.numpy.org), and [SciPy](https://www.scipy.org/scipylib/index.html), but no matplotlib.
- A partial list of interpreters out-of-the-box. If your favorite interpreter isn't included, consider [adding it with the api](http://zeppelin.incubator.apache.org/docs/0.6.0-incubating-SNAPSHOT/manual/dynamicinterpreterload.html).
  - spark
  - shell
  - angular
  - markdown
  - postgresql
  - jdbc
  - hive
  - hbase
  - elasticsearch
  - cassandra
  - R

A prior build of `dumontcyril/docker-zeppelin-r:latest` contained Spark 1.6.0, Python 2.7, and **all** of the stock interpreters.

## simple usage

To start Zeppelin pull the `latest` image and run the container:

```
docker pull dumontcyril/docker-zeppelin-r
docker run --rm --name zeppelin -p 8080:8080 dumontcyril/docker-zeppelin-r
```

Zeppelin will be running at `http://${YOUR_DOCKER_HOST}:8080`.

## complex usage

You can use [docker-compose](http://docs.docker.com/compose) to easily run Zeppelin in more complex configurations. See this project's `./examples` directory for examples of using Zeppelin with `docker-compose` to :

- read and write from local data files
- read and write documents in ElasticSearch

## license

MIT
