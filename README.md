# Fix Wordpress Permissions Script

For Debian:

Finding out which Apache user is running

```ps -ef | egrep '(httpd|apache2|apache)' | grep -v `whoami` | grep -v root | head -n1 | awk '{print $1}'```

Save the file as fix-wp.sh and set appropriate permissions for that script file using the following command: 

```chmod +x fix-wp.sh```

Run the script with the following command:

```./wordpress-perms.sh```

Bonus: ``` usermod -a -G www-data YourUserName ```
