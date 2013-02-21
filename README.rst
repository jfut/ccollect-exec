ccollect pre- and post- execution scripts
=========================================

post_check_daily_backup
-----------------------

* Check daily backup for a host:

::

  ./post_check_daily_backup HOSTNAME

* Check daily backup for hosts:

::

  ./post_check_daily_backup -a

* with post_exec:

::

  #/bin/sh
  WORK_DIR=$(dirname $0)
  # check daily backup
  ${WORK_DIR}/post_check_daily_backup ${name}

* with crontab:

::

  00 12 * * * /etc/ccollect/defaults/post_check_daily_backup -a >> /var/log/ccollect-check.log 2>&1

License
-------

* GPLv3

Other resources
---------------

* `ccollect - (pseudo) incremental backup with different exclude lists using hardlinks and rsync <http://www.nico.schottelius.org/software/ccollect/>`_
