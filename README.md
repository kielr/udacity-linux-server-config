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
- Added a user called "grader"
- Allowed sudo for user "grader" in /etc/sudoers.d/grader
- Updated/upgraded all installed packages
- Switched SSH default port to accept from 2200
- UFW config (Allow 2200 for SSH, Allow port 80 for HTTP)
- Configure time-zone with dpkg-reconfigure
- Disabled SSH login for root
- Allowed SSH for user grader, and user ubuntu
- Cloned item_catalog app into /var/www
- Configured a new virtual host in /etc/apache2/sties-available/catalog.conf
- Created "catalog" database in PSQL, created "catalog" user,

Summary of third party resources used to finish this project:
- Stackoverflow, a lot
