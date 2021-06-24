# docker-web-portal
This repo creates a web page that would take in and run docker commands. For demonstration follow this link: [docker-web-portal](https://www.linkedin.com/posts/bhardwaj-rahul_webportal-docker-python-activity-6813804107992715264-ZpFp)

## Prerequisites
* Install an httpd server on your Linux server.
* Copy the front.html and style.css file in ```/var/www/html```.
* Copy the back.py file in ```/var/www/cgi-bin```.
* Start the httpd services with ```systemctl start httpd```.
* As the server will be working with the privileges of Apache user there would be a few things you'll need to take care of:
* - In the ```/etc/groups``` folder add the apache group in your docker user by adding it after the third delimiter. The entry should look something like this: ```docker:x:973:apache```.
* - This step might not be necessary but if need arises, give some more privileges to the apache group in the ```/etc/sudoer``` file. Trying starting with giving the root powers.
* - Stop SELinux by ```setenforce 0```.

And that's it you're good to go!
