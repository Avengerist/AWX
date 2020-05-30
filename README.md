# AWX
<h2>Packages Installation</h2><br>

**Selinux should be disabled!**<br>

`yum install -y epel-release nano`<br>

`yum -y install git gcc gcc-c++ nodejs gettext device-mapper-persistent-data lvm2 bzip2 python-pip yum-utils python3-pip ansible`<br>

<h2>Installing Docker CE</h2><br>

`yum-config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo`<br>

`yum install -y docker-ce`<br>

`systemctl enable --now docker.service`<br>

`pip3 install docker-compose`<br>

<h2>Downloading AWX from Github</h2><br>

`git clone --depth 50 https://github.com/ansible/awx.git`<br>

<h2>Installation AWX</h2><br>

`cd /root/awx/installer/`<br>

`ansible-playbook -i inventory install.yml`<br>

<h2>Docker configuration</h2><br>

`docker ps`<br>

`docker exec -it $CONTAINER_ID /bin/bash`<br>

*Add records for **/etc/hosts** about **myowngitlab.com**<br>

`echo "IP_Address myowngitlab.com" >> /etc/hosts`<br>

<h2>AWX - WEB</h2><br>

Enter in Browser **ip_of_AWX** and login with creds:<br>

user: *admin*<br>
password: *password*<br>

<h2>Configuration for JOB</h2><br>

<h3>Credentials</h3><br>

1) Add some ***NAME***<br>
2) Choose a ***credential type***<br>
3) Type ***username*** & ***password***<br>
4) ***SAVE***<br>

<h3>Projects</h3><br>

1) Add some ***NAME***<br>
2) Choose ***SCM TYPE*** **Git**<br>
3) Choose ***SCM URL*** **myowngitlab.com....git**<br>
4) ***SAVE***

<h3>Inventory</h3><br>

1) Add some ***NAME***<br>
2) ***SAVE***<br>
3) Choose ***HOSTS***<br>
4) Add IP Of Client in ***HOST NAME*** <br>
5) ***SAVE***<BR>

----------------------------------------------------------<br>
**Create** own **playbook** and after do the next.<br>
----------------------------------------------------------<br>
<h3>Templates</h3><br>

1) Add some ***NAME***<br>
2) Choose ***VERBOSITY***<br>
3) Choose ***INVENTORY***<br>
4) Choose ***PROJECT***<br>
5) Choose ***PLAYBOOK**<br>
6) ***SAVE***<br>
7) ***LAUNCH***<BR>
