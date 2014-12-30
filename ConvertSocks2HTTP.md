ConvertSocks2HTTP
===========

1. download Privoxy, locate its config file in /usr/local/etc/privoxy/. 
2. Add Following line. This set all the request gets forwarded to privoxy. It also opens a random port of my machine to listen to it.

    forward-socks5 / 127.0.0.1:8899 . \n
    listen-address  0.0.0.0:3128    \n

3. Set npm config in sudo su - 
    npm config set proxy http://proxy.company.com:8080  \n
    npm config set https-proxy http://proxy.company.com:8080    \n

    npm config set proxy http://localhost:3128  \n
    npm config set https-proxy https://localhost:3128   \n

4. Remove
    npm config delete http-proxy    \n
    npm config delete https-proxy   \n
