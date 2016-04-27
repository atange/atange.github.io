这里是搜农作品的展示页以及学习资料整理的空间。
git命令行操作：
1、将本地仓库newDemoGit与GitHub上的远程库newDemoGit建立连接。
执行命令：
$ git remote add origin https://github.com/FeCheng/newDemoGit.git

2、将本地代码推送到远程库。
依次执行以下命令：
  $ git add .
  $ git commit -m "commit message"
  $ git push -u origin master  
会提示输入GitHub用户名，密码。填写您的用户名，密码即可。

3、 查看远程仓库
$ git remote -v
eoecn   https://github.com/eoecn/android-app.git (fetch)
eoecn   https://github.com/eoecn/android-app.git (push)
origin  https://github.com/com360/android-app.git (fetch)
origin  https://github.com/com360/android-app.git (push)
su@SUCHANGLI /e/eoe_client/android-app (master)
从上面的结果可以看出，远程仓库有两个，一个是eoecn，一个是origin

4、从远程获取最新版本到本地
$ git fetch origin master
From https://github.com/com360/android-app
 * branch            master     -> FETCH_HEAD
su@SUCHANGLI /e/eoe_client/android-app (master)
$ git fetch origin master 这句的意思是：从远程的origin仓库的master分支下载代码到本地的origin master

5. 比较本地的仓库和远程参考的区别
$ git log -p master.. origin/master
su@SUCHANGLI /e/eoe_client/android-app (master)
因为我的本地仓库和远程仓库代码相同所以没有其他任何信息

6、 把远程下载下来的代码合并到本地仓库，远程的和本地的合并
$ git merge origin/master
Already up-to-date.
su@SUCHANGLI /e/eoe_client/android-app (master)
我的本地参考代码和远程代码相同，所以是Already up-to-date

7、强制更新到远程仓库
$ git push --force origin master

以上的方式有点不好理解，大家可以使用下面的方式，并且很安全
