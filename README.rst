Tuenti exercises
================

Requirements
---------------
The requirements are the following:

    - python 2.7.9+
    - pip 10.0.1
    - virtualenv 12.0.7

# Step 1: Create and activate virtualenv

.. code:: console

    $ virtualenv tuenti-env
    $ source tuenti-env/bin/activate

# Step 2: Update pip  and install all dependencies:

.. code:: console

    $ python -m pip install --upgrade pip
    $ pip install -r requirements.txt

# Step 3: Could be necessary add the root path to PYTHONPATH.
It could be done using the following command in unix from the root path:

.. code:: console

    $ cd ../../tuenti-exercises # where  tuenti-exercises is the root path
    $ export PYTHONPATH=`pwd` # executed from the root path

Running Tests
-------------

Each folder contain a differente  automation code with differents frameworks:

**web**

    Within web folder we have 2 differents folder:
        **utils**
            Used to save a necessary code
        **tests**
            Here we've:
                - the variable python file saving the required variables
                - Folder **additional_tests**
                    Here are the additionals  tests. They can be executed using:
                        python test_profile.py
                - Folder **login**
                    The are the mandatory tests implemented
                        - Folder **tests**
                            There are the mandatory tests implemented with 3 differents testsuites which can be executed passing an argument as the following:
                                - python test_login suite_ok
                                - python test_login suite_nok
                                - python test_login empty_fields
                                - python test_login executes all tests
                            using testsSuite more tests can be added/deleted from each testsuite
                        - Folder **test_ddt**
                            There are the mandatory tests implemented using ddt framework which read dataset from the files:
                                - empties_login_dataset.csv
                                - successful_login_dataset.csv
                                - unsuccessful_login_dataset.csv

**web_behave**
As an extra effort, the mandatory login tests has been implemented using behave&Toolium framework too. This code has the following structure:
    - conf folder:
        The variables used are here. Such as driver path, implicitly_wait, url....
    - features:
        Features files with described scenarios are here
    - output:
        Logs will be saved here
    - PageObject:
        PageObjects implementes with toolium are here
    - Steps:
        Steps used in features files are here
They can be executed using the command:
    behave web_behave
