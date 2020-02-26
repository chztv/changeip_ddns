### 登入您的vps,

```wget -N --no-check-certificate "https://github.com/chztv/changeip_ddns/raw/master/ddns.sh" && chmod +x ddns.sh```


### 编辑 ddns.sh 文件

```nano /root/ddns.sh```
或者
```vi /root/ddns.sh```

### 修改此处内容为自己的

```
CIPUSER=您在ChangeIP登記的郵箱
CIPPASS=您在ChangeIP設定的密碼
CIPHOST=您在ChangeIP設定的域名
```

### 尝试运行一下
```bash /root/ddns.sh```

### 返回下面資訊即代表腳本正常
```
200 Successful Update
Old IP = 219.76.163.216
New IP = 220.246.88.57
Update Time = Sat Feb 8 22:11:04 CST 2020
Update Done.
```

### 設定定時更新

```crontab -e```

加入下列代码
```*/1 * * * * /root/ddns.sh >/dev/null 2>&1 &```
