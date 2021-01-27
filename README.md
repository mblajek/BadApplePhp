# BadApplePhp
Bad Apple in compact PHP
- scripts generate always a single frame of animation
- frame is based on current time, so every 1/16s next frame will be served
- to animate, continuous refreshing is needed, for now, works best in firefox
- availaible here, but please don't kill my server: http://mirkl.es/ba/
- there are two versions:

## simple.php
- frame is sent as standard output and script ends
- parses video data in each request, works fine with php-fpm
- can be used with webserver or in pure php
- run `php S- localhost:8080` in BadApplePhp directory and open `localhost:8080/simple.php`

## socket.php
- script creates single server by itself
- video data is parsed once, so it has really low requirements
- run `php socket.php` in BadApplePhp directory and open `localhost:8080/`

video data is based on Abaduaber's version: https://youtu.be/IXOVUiyx1a8
