# Virtual Host Documentation for Windows

## Overview

A virtual host is a method of hosting multiple domain names (or websites) on a single server. This is achieved by directing the incoming web traffic to different directories or locations on the server, based on the domain name requested by the user.

## Technology Used

- PHP 8.1.17
- MySQL
- XAMPP (Apache)

## Prerequisites

Before you begin, ensure you have the following installed:

- [XAMPP](https://www.apachefriends.org/index.html)
- Web browser (e.g., Chrome, Firefox)


## For Configuring Virtual Host
### 1. Create Web Page: 
Create a file on the web server's root directory (e.g., htdocs in XAMPP) with required extention (e. g., .php/.html).
### 2. Edit httpd-vhosts.conf:
If you are using XAMPP on Windows, this file is typically located in the apache\conf\extra directory within the XAMPP installation (e.g., 'C:\xampp\apache\conf\extra\httpd-vhosts.conf'). Open the file in the editor with administrative permission and add the following instructions.<br/>
```
      <VirtualHost *:80><br>
            DocumentRoot "C:/xampp/htdocs/folder_name/file_name.php"<br/>
            ServerName mywebsite.com<br/>
      </VirtualHost>
```
Adjust the DocumentRoot and ServerName as needed.
### 3. Edit hosts File
With administrator privileges, edit the 'C:\Windows\System32\drivers\etc\hosts' file using the following instructions.
```
      127.0.0.1      mywebsite.com
```
### 4. Restart Apache Server
Restart the Apache server in XAMPP to apply the changes.
### 5. Access Your Website
You've successfully set up virtual hosts on your server. you can use 'mywebsite.com' url to run your website.

## Note: 
Ensure to replace 'folder_name' with the actual folder name and adjust paths accordingly. Make sure you have administrative privileges when editing configuration files.
