simplesaml
==========
Webserver setup

'''
<VirtualHost *:80>
        ServerName saml.local
        DocumentRoot /Library/WebServer/Documents/simplesaml/www

        <Directory /Library/WebServer/Documents/simplesaml>
          AllowOverride all
          Order Deny,Allow
          Allow from all
        </Directory>
</VirtualHost>
'''
