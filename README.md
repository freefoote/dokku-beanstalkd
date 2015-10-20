# dokku beanstalkd

A simple beanstalkd plugin for Dokku.

It is based off the official Dokku Postgres plugin, with the exception
that it can't export or import data, as that doesn't make much sense for this.

## Environment

The target container gets an BEANSTALKD_URL environment variable in the format
beanstalkd://IP:PORT/, that you can use to connect inside your app.

Beanstalkd does not support authentication, so anyone who can connect can
access it. Be very careful if you choose to expose the port externally.

## Requirements

- dokku 0.4.0+
- docker 1.8.x

