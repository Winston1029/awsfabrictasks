.. _awsfab_settings:

======================================
awsfab_settings.py --- Settings
======================================


Required setup
==============
awsfabrictasks uses a settings system similar to the Django settings
module. You add your settings to ``awsfab_settings.py``.

Required configuration
----------------------
Create a file named ``awsfab_settings.py``, and add your AWS Security credentials::

    AUTH = {'aws_access_key_id': 'Access Key ID',
            'aws_secret_access_key': 'Secret Access Key'}

You find these under ``My account -> Security Credentials`` on
http://aws.amazon.com/.

.pem-key
--------
The ``.pem``-keys (key pairs) for you instances (the ones used for SSH login)
must be added to ``~/.ssh/`` or the current directory. You can change these directories
with the ``awsfab_settings.KEYPAIR_PATH`` variable (see :ref:`defaultsettings`).


Local override
==============
You may override settings in ``awsfab_settings_local.py``, which is typically
used to store authentication credentials outside your version control system
(i.e: with git you would add awsfab_settings_local.py to .gitignore).


.. _examplesettings:

Example awsfab_settings.py
==========================

.. literalinclude:: awsfab_settings_example.py



.. _defaultsettings:

Default settings
================

..
    ..literalinclude:: ../awsfabrictasks/default_settings.py

.. automodule:: awsfabrictasks.default_settings
