# autobackup
OpenVZ and raw backup via dedicated backup server with ZFS storage

```
# /opt/autobackup/autobackup --help
usage: autobackup [-h] --host HOST --type TYPE --dest PATH --save COUNT

optional arguments:
  -h, --help    show this help message and exit
  --host HOST   remote host to backup it on ZFS
  --type TYPE   remote host type: etc, raw, ovz
  --dest PATH   backup destination on local ZFS
  --save COUNT  count of saved backup snapshots
```

examples:

```
 # /opt/autobackup/autobackup --host=10.0.2.6 --type=etc --dest=/tank/backup/test-etc --save=30
 # /opt/autobackup/autobackup --host=10.0.2.6 --type=raw --dest=/tank/backup/test-raw --save=30
 # /opt/autobackup/autobackup --host=10.0.2.6 --type=ovz --dest=/tank/backup/10.0.2.6 --save=30
```
