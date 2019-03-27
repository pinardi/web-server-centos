## web-server-centos
create webserver di centos
1. Install Apache
```bash
sudo yum clean all
sudo yum -y update
sudo yum -y install httpd
```
2. allow apache trough firewall
a. Allow the default HTTP and HTTPS port, ports 80 and 443, through firewalld:
```bash 
sudo firewall-cmd --permanent --add-port=80/tcp
sudo firewall-cmd --permanent --add-port=443/tcp
```
b. And reload the firewall:
```bash
sudo firewall-cmd --reload
```
3. Configure Apache to Start on Boot
a. And then start Apache:
```bash
sudo systemctl start httpd
```
b. Be sure that Apache starts at boot:
```bash 
sudo systemctl enable httpd
```
4. Other useful commands for Apache 
a. To check the status of Apache:
```bash
sudo systemctl status httpd
```
b. To stop Apache:
```bash 
sudo systemctl stop httpd
```
