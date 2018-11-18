# The Little Wooden People Visits Colombia

## Production Environment configuration

Create an AWS Lightsail instance.

Create `conf` and `htdocs` folders in your project

`sudo mkdir /opt/bitnami/apps/little-wooden-poeple-colombia/conf`
`sudo mkdir /opt/bitnami/apps/little-wooden-poeple-colombia/htdocs`

Edit the `httpd-prefix.conf` file located in `/opt/bitnami/apps/myapp/conf/httpd-prefix.conf` and add the line below to it:

Include "/opt/bitnami/apps/little-wooden-people-colombia/conf/httpd-app.conf"

Create and edit the `httpd-app.conf` file located at `/opt/bitnami/apps/little-wooden-poeple-colombia/conf/httpd-app.conf` and add the content below to it. This is the main configuration file for your application, so modify it further depending on your application’s requirements.

`ProxyPass / http://127.0.0.1:1234/`
`ProxyPassReverse / http://127.0.0.1:1234/`

## Deployment steps

Each release to production implies a change of version. Version changes are managed with Git through the use of tags.

Pull your latest release from your source repository and restart the server.

https://medium.com/@sharmasha2nk/aws-lightsail-bitnami-nodejs-letsencrypt-cf653573b8a1
