# fsnd-linux-server-config

# README - Item Catalog Project for Udacity
Udacity Full Stack Web Developer Nanodegree Project : Linux Server Configuration

Server Public IP Address: http://3.84.174.94

Application url: http://ec2-3-84-174-94.compute-1.amazonaws.com

SSH Port: 2200

Private key for ubuntu user 'grader' provided in submission notes.

The password for this private key is 'Udacity101'.

---

## Software Installed: 

1. Ubuntu 18.04 Xenial - Operating System

2. Apache2 - Server Application

3. Postgresql - Database Application

4. Python 3.6.7 - Required to run Restaurants Menu Project. Ubuntu 18.04 comes with python3 pre-installed. Python 2.7 was installed in parallel.

5. Apache2 Module: mod_wsgi - The Restaurants Menu Project uses python and consequently apache2 requires the wsgi module to serve it.

6. Python Modules:

* psycopg2 - Not strictly required to run postgresql using sqlalchemy, but recommended by ubuntu package source lists.

* requests - Required to make API requests in python. Already installed with python.

* Oauth2client - Required for third-party authentication via Facebook and Google using Oauth2.

---

## Summary of Configurations Made:
1. As stated above, I started a new Ubuntu Linux server instance on Amazon Lightsail. 

2. Used Vim to make SSH easy by adding entries to my local SSH config file. 

3. Updated and upgraded all pre-installed software on the system using `sudo apt-get update` and `sudo apt-get upgrade`.

4. Configured the server by changing the SSH port from 22 to 2200. Made certain to configure the Lightsail firewall to allow it. 

5.  Designed the UFW firewall to only allow incoming connections on ports 80(HTTP), 123(NTP), and 2200(SSH). 

6.  Generated user 'grader' in Ubuntu (in order for the project to be reviewed). Gave this user sudo permissions. Created an SSH key pair locally for 'grader' and copied the public key into file /home/grader/.ssh/authorized_keys.

7. Set the local timezone to UTC (sudo timedatectl set-timezone UTC). 

8. Installed Apache2 and mod_wsgi.

9. Installed Postgresql and psycopg2. Established that remote connections were not allowed, and created a new database user named 'catalog' that has limited permissions. 

10. Installed git (was already installed with python3). 

11. Cloned and setup Restaurants Menu Project from Github. 

12. Updated everything using `sudo apt-get update` and `sudo apt-get upgrade`. Set up project in my server so that it functions correctly when visiting my server's IP address in a browser. 

---

## Third Party Resources:

- [Google+ API](https://developers.google.com/)

- [Facebook API](https://developers.facebook.com/)

- [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-create-a-sudo-user-on-ubuntu-quickstart) - Used to create a sudo user on Ubuntu.

- [Flask Deployment Options](http://flask.pocoo.org/docs/0.12/deploying/#deployment)

- [mod_wsgi (Apache)](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)
---



