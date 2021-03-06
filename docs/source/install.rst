
Installation
------------

Dependencies
^^^^^^^^^^^^

The current version of `gmaps` is only tested with *IPython 4.2* or later and *ipywidgets 5.1.3* or later. To upgrade to the latest versions, use::

    $ pip install -U jupyter

Make sure that you have enabled widgets extensions to Jupyter::

    $ jupyter nbextension enable --py --sys-prefix widgetsnbextension

Installing `gmaps`
^^^^^^^^^^^^^^^^^^

Install the Python component using::

    $ pip install gmaps

Then tell Jupyter to load the extension with::

    $ jupyter nbextension enable --py gmaps

Development version
^^^^^^^^^^^^^^^^^^^

You must have `NPM <https://www.npmjs.com>`_ to install the development version. You can install NPM with your package manager.

You must also install ``gmaps`` in a virtual environment (or, at least, you must be able to run ``pip`` without root access).

Clone the git repository by running::

    $ git clone https://github.com/pbugnion/gmaps.git

Change to the project's root directory and run::

    $ pip install -e .

This will create a directory called ``static/`` in the ``gmaps/`` directory. This directory contains Javascript sources. Every time you change the Javascript sources, you will need to recompile this directory by re-running this command (despite everying being installed in `editable` mode). 

You can then enable the extension in Jupyter::

    $ jupyter nbextension install --py --symlink --user gmaps
    $ jupyter nbextension enable --py --user gmaps

