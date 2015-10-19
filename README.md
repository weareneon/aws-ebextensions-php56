# aws-ebextensions-php56
Starter .ebextensions for php 5.6 projects



#### Password Protected Sites

By default, all environemts will have this enabled. To disable it on production, please add the following configuration variable:
```
AWS_ENV=production
```

To set a projects username & password, edit the line in ```.ebextensions/10_passwd.config```

You can create a new password by using the follinwg command on your CLI: ```htpasswd -bn username password```

This will output a new username:password line, that you can place into the config file.


#### nginx Rewrite Rules

Any Rewrite Rules should be placed in ```.ebextensions/02_rewrites.config```. Do not edit any of the other files. 
