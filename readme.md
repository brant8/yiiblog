###create a new repository on the command line
```
	echo "# yiiblog" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin git@github.com:brant8/yiiblog.git
	git push -u origin master
```
其他命令可能需要使用sudo命令，使用push反而不能使用sudo命令。

###push an existing repository from the command line
```
	git remote add origin git@github.com:brant8/yiiblog.git
	git push -u origin master
```
[参考CSDN](https://blog.csdn.net/u012526120/article/details/49401871)


### 设置GIT连接到Github:
	1.根据网络教程设置SSH密钥。
	2.遇到permission denied问题后，查看本目录权限，用户组权限chown。
	3.推送命令：
``
		git addd .
		git commit -m "message"
		git commit origin master
``

###1.遇见的问题
>>>Unable to write the file '/var/www/html/yiiblog/backend/models/User.php'.

文件夹controllers,models,views默认权限为drwxr-xr-x。




