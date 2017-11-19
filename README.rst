==========
autobackup
==========

OpenVZ and raw backup via dedicated backup server with ZFS storage

.. code-block:: bash

    # /opt/autobackup/autobackup --help
    usage: autobackup [-h] --host HOST [--port PORT] --type TYPE --dest PATH --save COUNT

    optional arguments:
      -h, --help    show this help message and exit
      --host HOST   remote host to backup it on ZFS
      --port PORT   remote port to backup it on ZFS
      --type TYPE   remote host type: etc, raw, ovz
      --dest PATH   backup destination on local ZFS
      --save COUNT  count of saved backup snapshots

Examples
--------

.. code-block:: bash

    # /opt/autobackup/autobackup --host=example.com --type=etc --dest=/tank/backup/example.com --save=30
    # /opt/autobackup/autobackup --host=example.net --type=raw --dest=/tank/backup/example.net --save=30
    # /opt/autobackup/autobackup --host=example.org --type=ovz --dest=/tank/backup/example.org --save=30

