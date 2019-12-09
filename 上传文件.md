利用git上传文件
===
下载一个git并安装
---
安装成功之后，输入以下命令，引号内的为你自己的名字和邮箱
```
git config --global user.name“your name"
git config --global user.email“ email@example.com” 
```
创建一个版本库，就是存放工程的地方
---
```
git init
```
把要上传的文件移动到此文件内和提交到创建的仓库内
---
···
git add.
git commit -m“自己对本次操作的命名”
···
配置ssh密钥
---
···
ssh-keygen -t rsa -C“自己的邮箱”
···
根据提示的地址找到id_rsa.pub，复制里面的代码
：githab点击用户，设置，SSH和GPG密钥，新的SSH密钥，将复制的代码粘贴。
```
ssh -t git@github.com（若不成功，则去掉-t参数）
```
提交
---
```
git remote add origin（你要上传的仓库地址）
git push -u origin master
```
