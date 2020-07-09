###Yii2傻瓜式使用教程
	Issue：使用`Composer`下载yii2,下载遇到`vendor`文件夹丢失。
	解决：使用`wget`下载yii2压缩包并进行解压。

###使用Git进行本地提交到Github
	使用SSH加密方式，步骤与网上一致。

###create a new repository on the command line
	```
	echo "# yiiblog" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin git@github.com:brant8/yiiblog.git
	git push -u origin master
	```

其他命令可能需要使用sudo命令，使用`push`反而不能使用sudo命令。

###push an existing repository from the command line

	```
	git remote add origin git@github.com:brant8/yiiblog.git
	git push -u origin master
	```
[参考CSDN](https://blog.csdn.net/u012526120/article/details/49401871)


### 设置GIT连接到Github:
	1.根据网络教程设置SSH密钥。
	2.遇到`permission denied`问题后，查看本目录权限，用户组权限`chown`还有`chmod`，根据实际情况更改权限。
	3.推送命令：

	```
		git addd .
		git commit -m "message"
		git commit origin master
	```

###1.遇见的问题

	使用Gii在Backend生成Post,Comment等文件。Gii需要开启`AllowedIPs`
	>Unable to write the file '/var/www/html/yiiblog/backend/models/User.php'.

	文件夹`controllers`,`models`,`views`默认权限为`drwxr-xr-x`。

###2.Backend,Frontend和Common的关系
	
	1.前后端都要使用的内容可以创造`model`在`common`命名空间下，然后使用继承方式在`Backend`下创建Post并更改为`extends common\models\Post`
	[参考链接](https://getyii.com/topic/720)
	2.为了减少代码视图，已有继承关系，把backend下`Post`内容全部`删除`。

###3.Post创建时间以及更新时间的插入

	使用`behaviors(){}`内置方法来进行快速操作。
	在`common\models\Post`添加`public function behaviors()`
	[参考](https://blog.csdn.net/qq_26656329/article/details/51852157)






