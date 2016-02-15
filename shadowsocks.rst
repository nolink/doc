================================
Shadowsocks
================================

Installation
============

Installation::
  
  $ yum install m2crypto python-setuptools
  $ easy_install pip
  $ pip install shadowsocks
  $ vi  /etc/shadowsocks.json
  :: 
  {
    "server":"0.0.0.0",
    "server_port":8388,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"iqunxingFx2015",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false,
    "workers": 1
  }


