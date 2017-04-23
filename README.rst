Toolium Examples
================

Set of examples to learn how to use `Toolium <https://github.com/Telefonica/toolium>`_ to test web, Android or iOS
applications, in different scenarios.

Getting Started
---------------

The requirements to install Toolium are `Python 2.7 or 3.3+ <http://www.python.org>`_ and
`pip <https://pypi.python.org/pypi/pip>`_. If you use Python 2.7.9+, you don't need to install pip separately.

Clone `toolium-examples <https://github.com/Telefonica/toolium-examples>`_ repository and install requirements. It's
highly recommendable to use a virtualenv.

.. code:: console

    $ git clone git@github.com:Telefonica/toolium-examples.git
    $ cd toolium-examples
    $ pip install -r requirements.txt

Running Tests
-------------

Each folder contains a sample project to test web using nose, behave or lettuce to execute
them.

By default, web tests are configured to run in chrome locally, so chrome must be installed in your machine and the
chrome driver must be downloaded and configured:

- Download `chromedriver_*.zip <http://chromedriver.storage.googleapis.com/index.html>`_
- Unzip file and save the executable in a local folder
- Configure driver path in *[Driver]* section in properties.cfg file ::

    [Driver]
    chrome_driver_path: C:\Drivers\chromedriver.exe


**web**

To run web tests with nose:

.. code:: console

    $ nosetests web

**web_behave**

To run behave web tests:

.. code:: console

    $ behave web_behave

**web_lettuce**

To run lettuce web tests:

.. code:: console

    $ lettuce web_lettuce

Note: lettuce works only in Python 2
