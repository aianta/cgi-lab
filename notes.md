# Connecting to WSL server from windows host

Run 
```
ifconfig
```
in WSL, then:
```
netsh interface portproxy add v4tov4 listenport=<port> listenaddress=0.0.0.0 connectport=<port> connectaddress=<your WSL IP>
```

From windows.

```
netsh interface portproxy add v4tov4 listenport=8080 listenaddress=0.0.0.0 connectport=8080 connectaddress=172.17.123.8
```

# Tunneling to lab machines

In OpenSSH, local port forwarding is configured using the -L option:
```
ssh -L 80:intra.example.com:80 gw.example.com
```
This example opens a connection to the gw.example.com jump server, and forwards any connection to port 80 on the local machine to port 80 on intra.example.com.

# Baking instructions
https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie

