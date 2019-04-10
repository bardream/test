# test:learn to use git
## 建立本地仓库
`cd /c/users/wrx/test`
`mkdir git_repository`

## 生成SSH密钥
`ssh-keygen -C 'yourmailaddress@mail.com' -t rsa`
按照提示完成创建/输入密码即可

- 如提示所示，以**记事本**打开密钥所在文件
- 将密钥复制到github账户的setting-SSH keys中
- 测试是否连接成功`ssh - T git@github.com`

## 创建一个项目
- 在github中`create repository`
- 在本地创建一个相同的项目
```
echo "# test" >>README.md
git init 	//初始化
git add README.md	//更新README文件
git commit -m "add README.md"	//提交更新并注释
git remote add origin https://github.com/bardream/test.git	//连接远程github项目
git push -u origin master	//将本地项目更新到github上去
```

若连接github项目时报错提示`fatal:remote origin already exists.`
解决方法：

`git remote rm origin`
后重新键入连接命令

## 初次尝试git到此为止啦！

另外git bash的下载在chrome下老是失败，建议用下载器下载。这里提供一个方案
## git下载失败解决方案

- 打开有下载连接的界面
- F12调出网站的JS代码
- `Ctrl+Shift+C`切换成可以通过点击网页元素并定位其代码的模式
- 点击下载链接，右侧代码中就可以定位到具体下载地址了，在下载器（eg迅雷）中打开，很快就下好了

## That's all

