# HTTP Basic Authentication Password Updater Web App

## Instruction

This web app is for the end users to change their password of HTTP Basic
Authentication themselves.

## Nginx Sub-URI config Example

```
location ^~ /<subpath> {
    # auth_basic              "Restricted";
    # auth_basic_user_file    /etc/nginx/passwd;
    proxy_pass              http://localhost:<port>/;
    proxy_connect_timeout 1;
    proxy_set_header        X-Script-Name     /<subpath>;
    proxy_set_header        Host              $http_host;
    proxy_set_header        X-Real-IP         $remote_addr;
    proxy_set_header        X-Forwarded-For   $proxy_add_x_forwarded_for;
    proxy_set_header        X-Forwarded-Proto $scheme;
}
```

## Demo

Here is a [demo](http://changyuheng.github.io/ba-pwd-updater/) without
functionality.

## License

Except where otherwise noted, all parts of this software is licensed under the
[MIT license](http://opensource.org/licenses/MIT).

© 2015 Chang Yu-heng
