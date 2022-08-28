# rpc-websocket-nginx
nginx reverse proxy for websocket EVM / Ethereum node rpc

## Insecure config (ONLY USE LOCALLY)

Install nginx webserver
> apt install nginx -y

> apt install npm nodejs -y

> npm install ws

Check if your node rpc / websocket is running and note the ports
> netstat -tulpen

Configure the websocket in ngix, add the websocket config in:
> /etc/nginx/sites-available

> systemctl restart nginx

> systemctl status nginx


Now start the node server.js using nohup (pm2 would be a better alternative for nohup)
> nohup node --no-warnings server.js &

Install wscat to test the websocket connection
> npm i wscat

> wscat --connect ws://192.168.100.101:9632

```
    connected (press CTRL+C to quit)
    > Hello Metaverse
    < Server received from client: Hello Metaverse
    > |
