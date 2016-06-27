## A simple PHP WebApp to run on an EC2 instance

### Usage
Lanunch an EC2 Instance with a public IP address, and the following User Data:

~~~~

#!/bin/bash
yum update -y
yum install httpd24 php56 git -y
service httpd start
chkconfig httpd on
cd /var/www/html
echo "<?php phpinfo();?>" > test.php
git clone https://github.com/nateforeman/awsstudent-first-ec2

~~~~

Then enter the following url in your web browser:

~~~~
http://[EC2 Instance Public IP]/awsstudent-first-ec2
~~~~
