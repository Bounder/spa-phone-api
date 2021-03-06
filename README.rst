=============
SPA Phone API
=============

SPA Phone API provides an API for Linksys/Sipura SPA IP Phones. It can be used
to programmatically update the phone's address book. Combining it into other
scripts it can be used to sync the phone's address book with (for example)
Google Contacts.

Installation
============

Installation with ``pip``:
::

    $ pip install spa-phone-api


Command Line Usage
==================

Update the address book from OS X Contacts. Defaults to sync all contacts, but
an optional group paramater can be specified.
::

    $ spa-sync ip-address [--group GROUP]

Usage
=====

Read the address book
::

    import spa_phone
    spa_phone.read('10.0.1.8')

Update the address book
::

    import spa_phone
    spa_phone.write('10.0.1.8', [
        ('Bouke Haarsma', '+31508200267'),
        ('WebAtoom', '+31508200267'),
        ('Apple Store', '+18006927753'),
    ])

Developing
==========

Accessing Outlook (Windows)
---------------------------
To access Outlook on Windows, you need ``pywin32``, which can be downloaded
from `sourceforge <https://sourceforge.net/projects/pywin32/files/pywin32/>`_.
Make sure to download the correct version matching your python version and
architecture. To install ``pywin32`` in your virtualenv, install it using
``easy_install`` in the activated virtualenv
::

    $ Scripts\activate.bat
    (env)$ easy_install [py2win]

Building EXEs (Windows)
-----------------------
To build EXEs on Windows, you need ``py2exe``, which can be downloaded from
`sourceforge <https://sourceforge.net/projects/py2exe/files/py2exe/>`_. The
same install instructions as ``pywin32`` apply.
