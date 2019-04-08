# Linux Server Configuration
*IP Addr:* 34.221.176.204

*URL:* http://ec2-34-221-176-204.us-west-2.compute.amazonaws.com/

Summary of software installed:
- Apache2
- Apache2
- mod_wsgi
- Python
- Python Pip
- Flask
- Virtual Env
- PostgreSQL

Summary of configurations made:
1. Created a user called `grader`
2. Allowed sudo for user `grader` in `/etc/sudoers.d/grader`
3. Updated/upgraded all installed packages
4. Switched SSH default port to accept from 2200 by editing `/etc/ssh/sshd_config` 
5. UFW config (Allow 2200 for SSH, Allow port 80 for HTTP, Allow 123 for NTP)
6. Copied the authorized_keys from the default `ubuntu` user to new user `grader`
  - `chmod 700 ~/.ssh` and `chmod 600 ~/.ssh/authorized_keys`
7. Configure time-zone with dpkg-reconfigure
8. Disabled SSH login for `root`
9. Allowed SSH for user `grader`, and user `ubuntu`
10. Restarted SSHD and SSH service
11. Cloned item_catalog app into `/var/www`
12. Configured a new `VirtualHost` in `/etc/apache2/sties-available/catalog.conf`
13. Created `catalog` database in PSQL, created `catalog` user,

Summary of third party resources used to finish this project: (I think there are more stackoverflow, but these are the ones I remember)
- https://stackoverflow.com/questions/7881469/change-key-pair-for-ec2-instance
- https://stackoverflow.com/questions/35017160/how-to-use-virtualenv-with-python
- https://stackoverflow.com/questions/21084791/flask-hello-world-using-apache-and-mod-wsgi-shows-files-in-webroot-only
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html
- https://unix.stackexchange.com/questions/257590/ssh-key-permissions-chmod-settings
- https://help.ubuntu.com/community/SSH/OpenSSH/Keys
