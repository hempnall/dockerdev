# NGINX Configuration

You must install ```apache2-utils```

Then create the password file...

```
# htpasswd -c <path_to_password_file> <username>
password: 12345
confirm_password: 12345
```

Then add users..

```
# htpasswd <path_to_password_file> <username>
```

Five users have been created

```
user1:user1pw
...
user5:user5pw
```
