devsup Package
==============

.. autofunction:: devsup.verinfo

:mod:`db` Module
----------------

.. module:: devsup.db

.. autofunction:: devsup.db.getRecord

:class:`Record` Class
^^^^^^^^^^^^^^^^^^^^^

.. class:: devsup.db.Record

    Allows access to a single record instance.
    *Record* instances can be created for any record in
    the process database.  However, some features will only
    function when the record has Python device support.
    
    *Record* objects allow access to fields through the
    :meth:`field` method and direct access to field
    values through attributes.
    
    Attribute access is currently limited to scalar fields.
    
    >>> R = getRecord("my:record:name")
    >>> F = R.field('VAL')
    >>> F.getval()
    42
    >>> R.VAL
    42
    >>> R.VAL = 43

    .. automethod:: name
    
    .. automethod:: rtype
    
    .. automethod:: field
    
    .. automethod:: scan
    
    .. automethod:: asyncStart
    
    .. automethod:: asyncFinish
    
    .. automethod:: info
    
    .. automethod:: infos

:class:`Field` Class
^^^^^^^^^^^^^^^^^^^^

.. autoclass:: devsup.db.Field

    .. automethod:: name

    .. autoattribute:: record

    .. automethod:: getval

    .. automethod:: putval

    .. automethod:: getarray

    .. automethod:: fieldinfo

.. autoclass:: devsup.db.IOScanListBlock
    :members:
    :inherited-members:
    :undoc-members:
    
.. autoclass:: devsup.db.IOScanListThread
    :members: add, interrupt


:mod:`hooks` Module
-------------------

.. automodule:: devsup.hooks
    :members:
    :undoc-members:
    :show-inheritance:

:mod:`util` Module
------------------

.. automodule:: devsup.util
    :members:
    :undoc-members:
    :show-inheritance:
