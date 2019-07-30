## Index

- Overview
- Setup
  - [Installing Certbot](#installing-certbot)
  - [Generating Certificates](#generating-certificates)
  - Editing Server Blocks
  - Fowarding non Https Traffic
- Testing

## Setup

###### Installing Certbot

Install Python and Common Software 
`apt-get install software-properties-common`  
Add in the Certbot Repository  
`add-apt-repository ppa:certbot/certbot`  
Update Apt Cache  
`apt-get update`  
Install Certbot  
`apt-get install certbot python-certbot-nginx` 

###### Generating Certificates  

Generate your first certificate, this certifacte will work for all listed sites. 
`sudo certbot --certonly --nginx --standalone -d example.com -d www.example.com`

When prompted, specify an administrative email address. This will allow you to regain control of a lost certificate and receive urgent security notices if necessary. 

Agree to the Terms of Service and specify if you would like to share your email address with E.F.F 
![Certbot t&cs](/images/certbot_run.png)

You will then get a notice confirming your newly generated certificates. 
The will go into `/etc/letsencrpyt/live/$server_name/` 
![Certbot certs](/images/certbot_cert.png)
