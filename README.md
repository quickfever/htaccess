- š Hi, Iām @quickfgit
- š Iām interested in Technology
- š± Iām currently learning line and graph
- š« How to reach me ohh no

<!---
quickfgit/quickfgit is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


# Redirect www to non-www

Usage
1. Trim www from your domain name.
2. Redirect www to non-www to fix Google Canonical issues.

Add this piece of code to your .htaccess file.

```
RewriteEngine On
RewriteCond %{HTTP_HOST} !^www. [NC]
RewriteRule ^(.*)$ http://www.%{HTTP_HOST}%{REQUEST_URI} [R=301,L]
```

# Redirect HTTP_HOST to HTTP_HOST

Add this piece of code to your .htaccess file.
RewriteEngine On
RewriteCond %{HTTPS}  !=on
RewriteRule ^/?(.*) https://%{SERVER_NAME}/$1 [R,L]
