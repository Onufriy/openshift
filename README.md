
<h1 align="center"> 免责声明 </h1>


<p align="center">
仅供科研学习之用，切勿用于其他用途
<br>
中国居民请自觉关闭本项目并24小时之内删掉与本项目相关的一切内容，否则出现一切问题，项目作者概不负责
</p>
<hr>


# v2ray 部署在 openshift

配置文件：
{
  "log": {
    "loglevel": "warning"
  },
  "inbound": {
    "protocol": "vmess",
    "port": 8080,
    "settings": {
      "clients": [
        {
          "id": "uuid换成你自己的",
          "alterId": 64,
          "security": "aes-128-gcm"
        }
      ]
    },
    "streamSettings": {
      "network": "ws"
    }
  },
  "inboundDetour": [],
  "outbound": {
    "protocol": "freedom",
   "settings": {}
  }
}



环境变量： CONFIG_JSON（配置）


用notepad++将上述变量中 \r\n 替换为\\n，变成一行，导入容器。






