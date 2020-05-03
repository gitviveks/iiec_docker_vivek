# Project - Blog/Article on WordPress container using MySQL container as a webserver host  
# Inroduction:
  With the rise of new technologies and idustries, old approach fails to stand strong where we have to wait so long (about 30-60mins) for setting up the new environment. There are multiple real cases where we have set the environment for a specific task, destroy it after use and again set lots of systems at large scale to deliver industry needs. It is hard to achieve it by normal way where we wait upto 1hr to launch a OS.
  Here Solomon Hykes came up with the idea of Docker where we can lauch any environment is just 1 second. Docker uses containerization technology for this. We have to set just configuration and docker will set it ready to use in just 1 second. Using this great technolgoy I developed a project under the mentorship of Mr. Vimal Daga Sir.
 This project based on multi-tier architecture and use concept of 
 
 # Requirements:
Bare Metal OS (Windows),
Virtualization Tool (Virtual Box),
Virtual Machine (RHEL 8),
Docker Tool,
Docker Images-
 1> mysql:5.7
 2> wordpress:5.1.1-php7.3-apache,
docker volumes-
 1> mysql_storage_new
 2> wp_storage_new
docker-compose

# Setting up the encironment
- First installed Virtual Box on windows as a virtualization tool. On the top of Vitual Box installed RHEL 8 OS
- In Red Hat 8 Docker CE is installed using a manul created repo as RHEL 8 does not support CE
  change directory  
  >cd /etc/yum.repos.d/
  
  create a file 
  >gedit docker.repo
  
  in that file put the following text.
  
  >[docker]
  >baseurl=https://download.docker.com/linux/centos/7/x86_64/stable/
  >gpgcheck=0
  
  after putting the above content in that file ,save that file and run following command
  >yum install docker-ce
  
  >systemctl enable docker
  
- Here docker is reday to use. I then installed appropriate MySQL and WordPress image
   >docker pull mysql:5.7
  
   >docker pull wordpress:5.1.1-php7.3-apache
