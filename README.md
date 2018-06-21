
# Linux-Server
### About
  This Project is about configuring the Linux-Server.

### Server Details

Server IP Address 13.232.124.125

Hosted site Url http://13.232.124.125.xip.io/

### How to connect as grader:

  save private key provided in your local machine and run the following command
  ```
  ssh -i path/to/privatekey -p 2200 grader@13.232.124.125
    
  ```
  
### Id_rsa key
```
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEA23fVmhK/YGrTbtq4uOGP2at7GqmpCiKWCnDMnmLHhRFrffvK
j/OG/fJq4o9rtCqzXmzUchnlJGhPaeRb+sJSsQJHc0MkdRDV3eVaXCq4ls3E6H2P
Bz06J165iTIsMpB7e3PRFrjwPe19vG/wob8GojiRpICX6y9FflKs/dLV6macC6TO
B0ijmGGGgMm8GHK7uRDz/W0MzoY34VygU7qWpRbRP77bWygWzI7oaMB3PrAjHER3
zF8cvzW3K7NfT1pfHtErcPSGCQCSxro/JdEIMLXbPVvRBsCo279Zj553ESlWe/+w
xWJ7F22t98CGDR3B1exwb+rwwNhAcfCaJd5VlQIDAQABAoIBAHIAhqFZGbZA54GO
9iN7b9jW/cR02w0buCrGO1QO5atWyCqSL7+k9btWQHVdoMne4HutNpHqp5/I22+b
IrhYVtIB6BGUkAyLaTyxlcWIn4gebSmDh1dwU5P93YzJ1jGR4cLX/4W5HXpdslG/
KBUtAIolrmnwLnoJfSTIV3omGd5+5c2FyJyvEafflSGw3AolrwMnhaPfd6wvDhZO
nx9I9DIBZUUoPppm2vCsjle+DcWK1GR9Bh9R9rVySgQlOVN6m901eQ+oNeVlDs8I
k8q7NIvTCytbE17eUD4gfZABfCph7W5DLGa/8OQxyeKN8HwkJOelSEZWbVsrq0gR
wMUxTyECgYEA/Ng25lRCS6FykrNexQXu1rsqOCPRSqKNyRqPS9JTpuGK21CS3X9g
vEOUSVmU4aTOp+OOx7b+lqfei2fMFoSV7dInvRRuyqv5OSXxHh5KrTtrQ505yvWs
8nfAuqgbsmPvdzHGwK0JX7M+e720Vm67ZG+fdmNV2Jd7fAoi0on3CIkCgYEA3jT9
Mh7JkLH1hlNcxQMliJiS+opc5y4IbttH7H+YxHEnfDaGOYgWF4s3WCq6Sw8xughp
7YDjcAJ5CYBV2I1gGCzKOxrTlM3nHFrwGyGoEJ+sQNfFU/NkC/a5lTUburLhXUjR
tQq6GfQ7AHj13dyZYzqnXddSOOI5UpBMWS/qya0CgYEA9Wv1VfrBYuHx8R10Rq+s
lfeUUmvJ0bUZBPPn1YPxOJHCE4ERHThvsC20eMIgNimfgezqgUZJtfh5lj0JJ25I
jVAozGpR5B2rSmJeuYpTl/SN+FJbb3qqBaxhgYx9XdmM7dh+ADW1XJQCeV+49RCE
ikeis+pVwGfBL7Qy+sN56mkCgYBIPhwPfnjz5Re5C0M+/i3mwgwPDorz0kCFoh85
IabOPyeiN6vd6oOcNfPRY1rb6l21aOTfhabsFLG7SBEg7Z3PXkiFfMxLNcIsstgb
Sg71EKSVFFGgYKInTZi6jOCuC1g/1tvvK0SkCYZhOfJdpknsO/aMCOQ/gDU4xZc8
69o+pQKBgQD6aarSlDdsXKIEXanDFjWIKo53e+Z7N82/usAf/9amF9O02RcndXc7
xAAyg0kawqjKv68pY76ovFiaDwfAdmZLhJ8Jm1ROv3EgFQAYBP7g8619VsccPq5F
f8mJamm3p1KcBo3PEbfRen1HJx2oHWmii2HqT78REPYhL9h/wrrTSw==
-----END RSA PRIVATE KEY-----
```
### passpharse password
'''
passpharse password is empty(you can directly press enter).


'''
### id_rsa.pub key
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDbd9WaEr9gatNu2ri44Y/Zq3saqakKIpYKcMyeYseFEWt9+8qP84b98mrij2u0KrNebNRyGeUkaE9p5Fv6wlKxAkdzQyR1ENXd5VpcKriWzcTofY8HPTonXrmJMiwykHt7c9EWuPA97X28b/ChvwaiOJGkgJfrL0V+Uqz90tXqZpwLpM4HSKOYYYaAybwYcru5EPP9bQzOhjfhXKBTupalFtE/vttbKBbMjuhowHc+sCMcRHfMXxy/Nbcrs19PWl8e0Stw9IYJAJLGuj8l0Qgwtds9W9EGwKjbv1mPnncRKVZ7/7DFYnsXba33wIYNHcHV7HBv6vDA2EBx8Jol3lWV lenovo@DESKTOP-79UK42Q

```
### grader password
```
ganesh

```
### Configuring Linux Server

#### Updating all packages
```
sudo apt-get update
sudo apt-get upgrade
```

#### Creating grader User:
  ```
  sudo adduser grader
  ```
  This will add new user
  ```
  sudo nano /etc/sudoers
  ```
  Below the Root user append the following line
  ```
  grader  ALL=(ALL:ALL) ALL
  ```
  This will grant sudo permission to grader
  #### Creating a ssh key pair for grader
   On your local machine in terminal/command prompt type
   ```
   ssh-keygen
   ```
   Which will generate the public and private ssh keys which is saved to .ssh folder
   
   Then in your virtual machine change to newly created user
   ```
   su - grader
   ```
   Create a new directory .ssh and new file authorized_keys in that directory
   ```
   mkdir .ssh
   sudo nano .ssh/authorized_keys
   ```
   Copy the public key with .pub extension to authorized_keys and save the file
   ```
   chmod 700 .ssh
   chmod 644 .ssh/authorized_keys
   ```
   - 700 will give read write and execute permission to user.
   - 644 prevent other user from writting in to file.
   Then restart ssh server
   ```
   service ssh restart
   ```
   
   Log in to grader with private key generated 
   ```
   ssh -i .ssh/id_rsa grader@ipaddress 
   ```
  #### Changing the ssh port to 2200
   ```
   sudo nano /etc/ssh/sshd_config
   ```
    
   Restart the ssh server
   
   ```
   service ssh restart
   ```
   
   >Note: Before Logging using ssh add custom TCP port 2200 under lightsaail firewall in networking tab in lightsail instance console  
   
   Now Login using command like this
   ```
   ssh -i .ssh/id_rsa -p 2200 grader@youripaddress
   ```
   
  #### Disabling ssh login as root
  `sudo nano /etc/ssh/sshd_config`
  
  make change `PermitRootLogin no`
  
  #### Configurating  Ufw firewall
  ```
  sudo ufw status
  sudo ufw allow 2200/tcp
  sudo ufw allow 80/tcp
  sudo ufw allow 123/udp
  sudo ufw enable
  ```
  This will allow all required ports and enables the ufw
  ```
  sudo ufw status
  ```
  It will display all allowed ports
  
  #### Changing time Zone
  `sudo dpkg-reconfigure tzdata`
  
  select none from list and then select utc.
  
  #### Installing Apache2 
  In terminal 
  
  ```sudo apt-get install apache2```
  
  Now mod_wsgi
  
  ```sudo apt-get install python-setuptools libapache2-mod-wsgi```
  
  Enable mod_wsgi
  
  ```sudo a2enmod wsgi ```
  ##### Setting up your flask application to work with apache2
   Creating a flask app
   
   In /var/www directory create a new folder
   `sudo mkdir FlaskApp`
   
   Install git 
   
   `sudo apt-get install git`
   
   move to the FlaskApp `cd FlaskApp`
   
   In that direcory clone your github repository
   
   `sudo git clone https://github.com/username/catalog.git`
   
   Rename your repository to FlaskApp
   
   Then rename your project file to `__init__.py`
   
   >Error : While accesssing the client_secrets.json file 
   ```
   PROJECT_ROOT = os.path.realpath(os.path.dirname(__file__))
   json_url = os.path.join(PROJECT_ROOT, 'client_secrets.json')
   CLIENT_ID = json.load(open(json_url))['web']['client_id']
   ```
   Use json_url instead client_secrets.json in script
   
  ##### Install and configuring postgresql for project
   Install Postgres `sudo apt-get install postgresql`
   
   login to postgres `sudo su - postgres`
   
   postgres shell `psql`
   
   create user `CREATE USER catalog WITH PASSWORD 'password';`
   
   permit user to createdb `ALTER USER catalog CREATEDB;`
   
   Create a db name  catalog with user catalog `CREATE DATABASE catalog WITH OWNER catalog;`
   
   connect to db `\c catalog`
   
   revoke all permission to public `REVOKE ALL ON SCHEMA public FROM public;`
   
   Give schema permission to user catalog `GRANT ALL ON SCHEMA public TO catalog;`
   
   exit from db and postgres `\q and exit`
   
   Change the database connection in both db_setup.py and `__init__.py` as `engine =       create_engine('postgresql://catalog:password@localhost/catalog')`
   
   Now you are ready with your applicatiom
  #### Configure and Enable a New Virtual Host
   `sudo nano /etc/apache2/sites-available/FlaskApp.conf`
   
   In this add the following code
   ```
   <VirtualHost *:80>
		ServerName mywebsite.com
		ServerAdmin admin@mywebsite.com
		WSGIScriptAlias / /var/www/FlaskApp/flaskapp.wsgi
		<Directory /var/www/FlaskApp/FlaskApp/>
			Order allow,deny
			Allow from all
		</Directory>
		Alias /static /var/www/FlaskApp/FlaskApp/static
		<Directory /var/www/FlaskApp/FlaskApp/static/>
			Order allow,deny
			Allow from all
		</Directory>
		ErrorLog ${APACHE_LOG_DIR}/error.log
		LogLevel warn
		CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
   ```
   Enable the virtual host 
   `sudo a2ensite FlaskApp`
   
   Disabling the default apache2 page
   `sudo a2dissite 000-default.conf`
   
  #### Create the .wsgi File
    ```
    cd /var/www/FlaskApp
    sudo nano flaskapp.wsgi 
    ```
   Add the following code
   
   ```
   #!/usr/bin/python
    import sys
    import logging
    logging.basicConfig(stream=sys.stderr)
    sys.path.insert(0,"/var/www/FlaskApp/")

    from FlaskApp import app as application
    application.secret_key = 'Add your secret key'
   ```
   save and exit
   
   Deploying flask app with apache2 is referred from [Digital ocean](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
   
   #### Installing require modules
   You can either install all modules on your machine or create a virtual environment for the project and install the modules
   ` pip install flask sqlalchemy psycopg2 requests oauth2client`
   
   #### Setting up your Google Oauth2
   Login to your [developer console](https://console.developers.google.com) and select your project and edit OAuth details as following
   
   Javascript origin
   `http://ip.xip.io`
   
   redirect URI
   
   `http://ip.xip.io/login`
   
   `http://ip.xip.io/gconnect`
   
   `http://ip.xip.io/callback`
   
   [xip.io](xip.io) is a free DNS which will be the same as using IP address
   
   #### Final Step
   Restart your apache2 server
   
   `sudo service apache2 restart`
