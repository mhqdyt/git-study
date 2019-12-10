git重置
===
重置（回滚到上次的提交）
---
利用reset来重置
```
git reset --hard 9aa22c0
```
而9aa22c0表示目录地址，为16进制来源于上次commit提交时产生的 git commit -m "img" [master 9aa22c0] img
查看文件的位置
---
```
git hash -object file.txt
```
执行这个语句会得到一串16进制的号码比如9aa22c0bc7b0ecbcacb0f5b69c9c14ecf191d8f4，这串16进制就是地址
查看文件内容
---
```
git cat-file -p c9a2be
```
c9a2be是文件的地址

查看文件类型,用-t
---
```
git cat-file -t c9a2be
```
查询提交了几次
---
```
git log --oneline
```
查看文件的结构（七位）
---
```
git cat-file -p 3b07a3b
```
会的到类似的笔记 100644 blob 38eb305e2c93b8ec8509a99686eb5383067be316 readme.txt 040000 tree 3c7ecf3378c8358244bdc0d73dfc06fb3a341241 src

查看 readme.txt的内容(五位)
---
```
git cat-file -p 38eb3
```
查看src文件（五位）
---
```
git cat-file -p 3c7ec
```
这两个的查看的文件的地址的16进制都是上面的地址前五位 100644 blob 38eb305e2c93b8ec8509a99686eb5383067be316 readme.txt 040000 tree 3c7ecf3378c8358244bdc0d73dfc06fb3a341241 src
