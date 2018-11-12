# Charles-for-Https

##### 1. Charles安装
[官网下载安装](https://www.charlesproxy.com/download/)

##### 2.HTTP抓包

###### （1）查看电脑IP地址
![](/images/charles-1.png)

###### （2）查看电脑IP地址
手机连上电脑，点击“设置->无线局域网->连接的WiFi”，设置HTTP代理：
服务器为电脑IP地址：如192.168.1.169
端口：8888

![](/images/charles-2.png)

设置代理后，需要在电脑上打开Charles才能上网

手机上打开某个App或者浏览器什么的，如果不能上网，检查前面步骤是否正确

![](/images/charles-3.png)

点击“Allow”允许，出现手机的HTTP请求列表

![](/images/charles-4.png)

##### 3. HTTPS抓包
HTTPS的抓包需要在HTTP抓包基础上再进行设置
设置前抓包HTTPS是这样的

![](/images/charles-5.png)

设置后抓包HTTPS长这样

![](/images/charles-6.png)


###### （1）安装SSL证书到手机设备

点击 Help -> SSL Proxying -> Install Charles Root Certificate on a Mobile Device

![](/images/charles-8.png)

出现弹窗得到地址 chls.pro/ssl

![](/images/charles-9.png)

在手机Safari浏览器输入地址 chls.pro/ssl，出现证书安装页面，点击安装
手机设置有密码的输入密码进行安装

![](/images/charles-10.png)

【注意】1、Safari浏览器输入这个网址chls.pro/ssl安装不了证书的情况,
       2、iOS 10.3系统，需要在 设置→通用→关于本机→证书信任设置 里面启用完全信任Charles证书

###### （2）Charles设置Proxy
Proxy -> SSL Proxying Settings...

![](/images/charles-11.png)

勾选Enable SSL Proxying,点击Add

![](/images/charles-12.png)

Host设置要抓取的https接口，比如想抓这个

![](/images/charles-13.png)

Host填写：https://api.weibo.cn
Port填写：443

![](/images/charles-14.png)

###### （3）进行HTTPS抓包

让手机重新发送https请求，可看到抓包

![](/images/charles-15.png)




