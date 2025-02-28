.. _commands-barman-generate-manifest:

``barman generate-manifest``
""""""""""""""""""""""""""""

Synopsis
^^^^^^^^

.. code-block:: text
    
    generate-manifest SERVER_NAME BACKUP_ID

Description
^^^^^^^^^^^

Generates a ``backup_manifest`` file for a backup. You can use a shortcut instead of
``BACKUP_ID``.

Parameters
^^^^^^^^^^

``SERVER_NAME``
    Name of the server in barman node

``BACKUP_ID``
    Id of the backup in barman catalog.

.. only:: man

    Shortcuts
    ^^^^^^^^^

    Use shortcuts instead of ``BACKUP_ID``.

    .. list-table::
        :widths: 25 100
        :header-rows: 1
    
        * - **Shortcut**
          - **Description**
        * - **first/oldest**
          - Oldest available backup for the server, in chronological order.
        * - **last/latest**
          - Most recent available backup for the server, in chronological order.
        * - **last-full/latest-full**
          - Most recent full backup eligible for a block-level incremental backup using the
            ``--incremental`` option.
        * - **last-failed**
          - Most recent backup that failed, in chronological order.