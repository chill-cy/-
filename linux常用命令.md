# linux常用命令

----

## 免密登录

| 执行顺序 | 命令                                        | 作用                     |
| :------- | ------------------------------------------- | ------------------------ |
| １       | ssh-keygen                                  | 创建密钥对               |
| ２       | ssh user@hostname                           | 远程登录user用户的主机   |
| ３       | ssh-copy-id user@hostname                   | 拷贝公钥到其他的主机地址 |
| ４       | scp user@hostname:/文件地址　本机的目录地址 | 将远程文件拷到本机目录下 |
| ５       | scp 本机目录地址　user@hostname:/文件地址   | 将本机文件拷到远程目录下 |



-----

##  常用命令

| 名称      | 用法                                                       | 作用                                                         |
| --------- | ---------------------------------------------------------- | ------------------------------------------------------------ |
| logout    |                                                            | 进超管后返回到普通用户                                       |
| tree      |                                                            | 以树形结构显示目录下内容                                     |
| pwd       |                                                            | 显示当前工作目录的绝对路径                                   |
| su        | `root@` 超管的家目录，输入管理员密码                       | 登录root                                                     |
| echo      | `echo $HOME`或`echo $PATH`或`echo $?`                      | 打印当前家目录；打印路径；上一条指令是否执行成功             |
| touch     | touch a                                                    | 新建一个空白文件，若原来有则不新建                           |
| sudo -i   | 普通用户输入用户密码                                       | 临时登录进管理员权限                                         |
| sudo      |                                                            | 临时获取管理员权限                                           |
| cp        | cp -r复制目录，cp A B                                      | 拷贝A文件到B目录下                                           |
| rm        | rm test.c ,rm -rf删除不提醒                                | 删除test.c文件                                               |
| man       | man ls                                                     | 查看命令具体用法                                             |
| mv        |                                                            | 移动文件                                                     |
| ls        |                                                            | 查看当前目录下的内容                                         |
| fg        |                                                            | 回前台                                                       |
| chmod     | chmod a+x 加权限                                           | 修改权限                                                     |
| ifconfig  |                                                            | 查看ip地址                                                   |
| awk       |                                                            |                                                              |
| cd        | `cd 当前目录下的目录`，`cd ~zy`                            | 打开目录, '~'直接到zy目录                                    |
| cat       |                                                            | 查看文件内容输出到终端                                       |
| apt-get   | `apt-get install nmon`                                     | 安装（相当于软件管家)， 一级命令apt-get， 二级命令install，参数nmon; 二级命令：updata更新源，upgrade更新版本 |
| apt-cache | `apt-cache depends nmon`或`apt-cache search aaa |grep aaa` | apt-cashe缓存文件；search信息检索; depends查看依赖的文件包；对信息进行检索'aaa'; |

----

## github上传命令

| 命令                                                         | 作用                                                        |
| ------------------------------------------------------------ | ----------------------------------------------------------- |
| git init                                                     | 在本地初始化仓库                                            |
| git status                                                   | 查看git的状态                                               |
| `git remote add orign git@github.com:chill-cy/CPractice.git` | 远程添加当前仓库和远程仓库连接                              |
| `git add 文件名`或`git add *`                                | add 跟踪文件,后者跟踪全部文件                               |
| git commit -m "备注"                                         | 提交到git                                                   |
| git push -u origin master                                    | 用git将提交的文件推到远程仓库的主分支，第一次提交要加-u选项 |
| git pull                                                     | 将远程仓库更改后的文件拉回                                  |
| git remote -v                                                | 显示对应的克隆地址，查看当前是否连接                        |

-----

## 选项命令

| 选项      | 用法                      | 作用                                      |
| --------- | ------------------------- | ----------------------------------------- |
| -x        | chmod a+x                 | x执行权限，chmod a+x 给所有文件加执行权限 |
| -a        | ls -a                     | 显示隐藏文件                              |
| -l        | ls -l                     | 竖向列出文件或目录的具体信息              |
| -F        | ls -F                     | 查看目录中的文件                          |
| \*[0-9]\* | ls \*[0-9]*               | 显示包含数字的文件名或数字名              |
| -purge    | apt -purge remove a       | 清除用户信息和配置信息，相当于全部卸载    |
| -f        | `apt-get install -f nmon` | 主动提醒                                  |

