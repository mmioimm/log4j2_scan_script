# log4j2_scan_script
此脚本修改自：https://github.com/fullhunt/log4j-scan

> 主要添加了内网检测功能，使用于内网不出网环境，无法获取dnslog的情况

> 修改默认参数：1. 发包默认方式改为POST 2. dns服务默认改为dnslog.cn

usage:

1. 基于dnslog.cn

   python3 log4j-scan.py -u http://www.xxx.com
2. 基于内网检测
   - 内网启动ldap服务：java -jar jndi.jar -i 127.0.0.1
   - python3 log4j-scan.py -u http://xxx.com --local-ldap 1
