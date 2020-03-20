# macOS上Git和GitHub的基本使用方法
## git常用操作
> git add --all   
> git commit -m "msg"   
> git push -u origin master   
## 第一节: 生成并获取密钥(本节操作均在终端中进行)
* STEP 1: 生成密钥。   
执行以下命令:(其中email address为注册GitHub时的邮箱地址)   
```
ssh-keygen -t rsa -C email address
```
执行命令后需按几次enter(回车键)   
其中，终端的部分输出如下:   
```
Your identification has been saved in ..
```
* STEP 2: 获取密钥。   
执行以下操作:(..的内容请留意上一节提到的终端的输出)   
```
cd ../.ssh
vi id_rsa.pub
```
此后，复制id_rsa.pub中的内容。接着，按esc键，再按ZZ键，以保存并退出，本节结束。   
## 第二节: 添加密钥(本节操作均在网页中进行)   
* STEP 3: 登陆GitHub   
* STEP 4: Github中添加密钥   
1. 添加密钥的路径: Setting => SSH and GPG keys => New SSH key   
2. 将id_rsa.pub中的内容粘贴到文本框，点击Add SSH key按钮   
## 第三节: 测试连接   
STEP 5: 执行以下命令以测试连接:   
```
ssh -T git@github.comssh -T git@github.com
```
若有以下输出，则说明连接成功:   
```
... You've successfully authenticated ...
```
## 第四节: 上传测试   
STEP 6: 创建Repositories   

STEP 7: 添加文件
执行以下命令:
```
git add file
```
STEP 8: 添加到暂存
执行以下命令:
```
git commit -m "file"
```
STEP 9: 上传
执行以下命令:
```
git push origin master
```
补充:若该目录第一次使用版本控制,则需在第8步和第9步之间插入以下操作:
```
git remote add origin HTTPS/SSH
```

