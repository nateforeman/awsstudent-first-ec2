# A simple PHP WebApp for aws students to run on an EC2 instance

## Usage
Lanunch an EC2 Instance with the following User Data:

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
