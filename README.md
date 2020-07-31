Setup Satellite
=========

This role is designed to setup a disconnected Satellite server.

Requirements
------------

For this role to work, you must provide a RHEL 7 Server, and Satellite 6 install DVDs.  Those ISO files should be placed in the files/ directory.
As of right now you will also need a tarball of ansible and sat-maintenance repos.  Until I refine exactly which packages are needed, the repos are too big to put in this role.

Role Variables
--------------

You must override the default varialbes for sat_iso and rhel_iso to reflect the iso files you placed in the files/ directory.  You will also need to update the tar_file repo to reflect the tarball you create of the extra required repos.
Default varialbes for size of filesystems are created in the defaults/main.yml.  These reflect the current disconnected install guide for Satellite at the time the role was created.  It is assumed your system already has a /var/log with at least 10G as required per the Satellite install guide.


Author Information
------------------

Created by: Charles Randall
email: chrandal@redhat.com