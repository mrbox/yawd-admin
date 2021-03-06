Installing yawd-admin
=====================

.. _prerequisites:

Prerequisites
+++++++++++++

yawd-admin requires that the `oauth2client` library is installed in your python environment::
	
	$ pip install oauth2client

If you plan to use the yawd-admin google analytics functionality, 
the `google-api-python-client` must also be installed::

	$ pip install google-api-python-client
	
yawd-admin is tested with django 1.4. Older django versions are not 
supported. 

.. _installation:

Application installation
++++++++++++++++++++++++

Install yawd-admin either from `pypi <http://pypi.python.org/pypi/yawd-admin/>`_
or the `github repository <https://github.com/yawd/yawd-admin/>`_::

	$ pip install yawd-admin
   
...or::

	$ git clone https://github.com/yawd/yawd-admin
	$ cd yawd-admin
	$ python setup.py install
	
Either ways all :ref:`prerequisites` (**except** from `google-api-python-client`)
will be automatically installed.

Since yawd-admin is actively being developed the github version is generally 
preferred; it contains all latest updates & fixes.
	
.. _demo-project:

Install the demo project
++++++++++++++++++++++++

In the demo project you will find a full example of yawd-admin (only the
google analytics functionality is not demonstrated).

Create a new environment named *yawdadmin* and activate it::

   $ virtualenv /www/yawdadmin
   $ source /www/yawdadmin/bin/activate
   
Download and install yawd-admin::

   $ git clone https://github.com/yawd/yawd-admin
   $ cd yawd-admin
   $ python setup.py install
   
At this point, yawd-admin will be in your ``PYTHONPATH``. Now initialize 
the example project::
   
   $ cd example_project
   $ python manage.py syncdb
   
When promted, create an admin account. Finally, start the web server::

   $ python manage.py runserver
   
...and visit *http://localhost:8000/*
to see the admin interface and experiment with its features.

.. note::
	The demo admin URLs are registered in the root url and no
	prefix (e.g. '/admin/') is needed.
	
Explore the demo project source code and read the comments, to better
understand how to use yawd-admin.

Once you are done, you can deactivate the virtual environment::

   $ deactivate yawdadmin