使用方法：
Step 1
curl https://raw.githubusercontent.com/sasoncheung/CloudFlareDDNS/master/cf-ddns.sh > /usr/local/bin/cf-ddns.sh && chmod +x /usr/local/bin/cf-ddns.sh

Step 2
vim /usr/local/bin/cf-ddns.sh

Step 3
CFKEY=API ID
CFUSER=E-mail
CFZONE_NAME=一级域名
CFRECORD_NAME=二级域名全名
保存，退出

Step 4
/usr/local/bin/cf-ddns.sh

Step 5
加入定时任务
crontab -e
添加一行
*/1 * * * * /usr/local/bin/cf-ddns.sh >/dev/null 2>&1

保存退出
