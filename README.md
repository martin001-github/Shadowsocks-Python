# Shadowsocks-Python

# execute command below
chmod +x shadowsocks.sh
./shadowsocks.sh 2>&1 | tee shadowsocks.log

# display as below after shell run
Congratulations, shadowsocks install completed!
Your Server IP:your_server_ip
Your Server Port:8989
Your Password:your_password
Your Local IP:127.0.0.1
Your Local Port:1080
Your Encryption Method:aes-256-cfb

Welcome to visit:http://teddysun.com/342.html
Enjoy it!

# uninstall
./shadowsocks.sh uninstall

# path after installation
/etc/shadowsocks.json

# single mode
{
    "server":"your_server_ip",
    "server_port":8989,
    "local_address":"127.0.0.1",
    "local_port":1080,
    "password":"yourpassword",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}

# multi-user mode
{
    "server":"your_server_ip",
    "local_address": "127.0.0.1",
    "local_port":1080,
    "port_password":{
         "8989":"password0",
         "9001":"password1",
         "9002":"password2",
         "9003":"password3",
         "9004":"password4"
    },
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}

# related command
#startup
/etc/init.d/shadowsocks start
#stop
/etc/init.d/shadowsocks stop
#restart
/etc/init.d/shadowsocks restart
#status
/etc/init.d/shadowsocks status
