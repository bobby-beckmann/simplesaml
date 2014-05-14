simplesaml
==========
Webserver setup

```
<VirtualHost *:80>
        ServerName saml.local
        DocumentRoot /Library/WebServer/Documents/simplesaml/www

        <Directory /Library/WebServer/Documents/simplesaml>
          AllowOverride all
          Order Deny,Allow
          Allow from all
        </Directory>
</VirtualHost>
```

Remember to add a saml.local to your localhosts.

For the community configuration:
```
Enable SAML: YES
Assertion Consumer service URL:  http://start.bloomfire.com:3000/auth/saml/callback
IdP SSO Target URL: http://saml.local/saml2/idp/SSOService.php
Issuer: http://croz.bloomfire.com
Name Identifier format: urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress
IdP Certificate fingerprint: D1:BA:B0:17:66:6D:7F:42:7B:91:1E:22:7E:3A:27:D2
IdP Certificate:
-----BEGIN CERTIFICATE-----
MIICgTCCAeoCCQCbOlrWDdX7FTANBgkqhkiG9w0BAQUFADCBhDELMAkGA1UEBhMC
Tk8xGDAWBgNVBAgTD0FuZHJlYXMgU29sYmVyZzEMMAoGA1UEBxMDRm9vMRAwDgYD
VQQKEwdVTklORVRUMRgwFgYDVQQDEw9mZWlkZS5lcmxhbmcubm8xITAfBgkqhkiG
9w0BCQEWEmFuZHJlYXNAdW5pbmV0dC5ubzAeFw0wNzA2MTUxMjAxMzVaFw0wNzA4
MTQxMjAxMzVaMIGEMQswCQYDVQQGEwJOTzEYMBYGA1UECBMPQW5kcmVhcyBTb2xi
ZXJnMQwwCgYDVQQHEwNGb28xEDAOBgNVBAoTB1VOSU5FVFQxGDAWBgNVBAMTD2Zl
aWRlLmVybGFuZy5ubzEhMB8GCSqGSIb3DQEJARYSYW5kcmVhc0B1bmluZXR0Lm5v
MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDivbhR7P516x/S3BqKxupQe0LO
NoliupiBOesCO3SHbDrl3+q9IbfnfmE04rNuMcPsIxB161TdDpIesLCn7c8aPHIS
KOtPlAeTZSnb8QAu7aRjZq3+PbrP5uW3TcfCGPtKTytHOge/OlJbo078dVhXQ14d
1EDwXJW1rRXuUt4C8QIDAQABMA0GCSqGSIb3DQEBBQUAA4GBACDVfp86HObqY+e8
BUoWQ9+VMQx1ASDohBjwOsg2WykUqRXF+dLfcUH9dWR63CtZIKFDbStNomPnQz7n
bK+onygwBspVEbnHuUihZq3ZUdmumQqCw4Uvs/1Uvq3orOo/WJVhTyvLgFVK2Qar
Q4/67OZfHd7R+POBXhophSMv1ZOo
-----END CERTIFICATE-----
```




It should point to saml.local now for login. A simple login is employee/employeepass. You can edit config/authsources.php to change your email address, etc.


