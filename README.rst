=====================
python-docker-machine
=====================

DISCLAIMER
============

**UNMAINTAINED/ABANDONED CODE / DO NOT USE**

Due to the new EU Cyber Resilience Act (as European Union), even if it was implied because there was no more activity, this repository is now explicitly declared unmaintained.

The content does not meet the new regulatory requirements and therefore cannot be deployed or distributed, especially in a European context.

This repository now remains online ONLY for public archiving, documentation and education purposes and we ask everyone to respect this.

As stated, the maintainers stopped development and therefore all support some time ago, and make this declaration on December 15, 2024.

We may also unpublish soon (as in the following monthes) any published ressources tied to this project (eg: pypi, dockerhub, the repositories, etc.).
So, please don't rely on it after March 15, 2025 and adapt whatever project which used this code.


Pythonic wrapper around docker-machine


installation
------------

::

    $ python setup.py install


or::

    $ pip install python-docker-machine



usage
-----

.. image:: https://readthedocs.org/projects/python-docker-machine/badge/?version=latest
   :target: http://python-docker-machine.readthedocs.org/en/latest/?badge=latest
   :alt: Documentation Status

::

     import machine
     import docker
     m = machine.Machine(path="/usr/local/bin/docker-machine")
     client = docker.APIClient(**m.config(machine='default'))
     client.ping()



requirements
------------

docker-machine on your system path

https://docs.docker.com/machine/install-machine/


running the test suite
----------------------

Make sure docker-machine is available on your system path. Next you need to create a docker machine with the name
``python-docker-machine`` with the driver of your choice, for example the virtualbox driver::

   $ docker-machine create -d virtualbox python-docker-machine


Now you can run the tests with nose::

    $  nosetests
    ......................
    ----------------------------------------------------------------------
    Ran 22 tests in 0.262s

or with tox::

    $ tox

