# frpc
Document: [https://github.com/fatedier/frp/blob/master/README.md](https://github.com/fatedier/frp/blob/master/README.md)

# how to use
```
$ mkdir /opt/frpc/config

$ cat > /opt/frpc/config/frpc.ini << EOF
# frpc.ini
[common]
server_addr = x.x.x.x
server_port = 7000

[ssh]
type = tcp
local_ip = 127.0.0.1
local_port = 22
remote_port = 6000
EOF

$ docker run --name frp-client --restart=always -v /opt/frpc/config:/conf -d pengpan/frpc
```
