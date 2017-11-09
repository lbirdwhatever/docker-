- 1.启动docker：systemctl start docker
- 2.列出本地镜像：docker images -a（全部） -f（过滤后面的）-q（镜像ID）--help
- 3.列出运行中的容器：docker ps -a（全部列出，包括未运行的）-f（过滤） -n（n是整数，列出最近安装的n个容器） -l（最近安装的容器） -q（容器ID）-s（显示所有文件即容器大小）
- 4.从docker hub中搜索符合条件的镜像：docker search sth -s 40（收藏数不小于40）
- 5.运行容器并进入：docker run -i -t ubuntu /bin/bash
- 6.启动容器：docker start ID -i（启动后，进入交互模式）
- 7.重启容器：docker restart ID
- 8.杀死进程：docker kill ID
- 9.容器停止运行：docker stop ID -t 10（超过10秒未启动，自动杀死进程）
- 10.删除容器：docker rm ID -f（强制删除）-l（移除容器间的网络连接）-v(移除与容器关联的空间)
- 11.删除镜像：docker rmi ID -f（强制删除）
- 12.查看制定镜像的创建历史docker history image's-name
- 13.查看版本信息：docker version 
- 14.显示系统信息，镜像数，容器数：docker info
- 15.从docker hub上拉取或更新指定镜像：docker pull sth -a（拉取所有带sth关键字的镜像）
- 16.在docker hub注册用户名邮箱密码即可：docker login
- 17.登出：docker logout
- 18.从服务器拉取个人动态：docker events
- 19.将指定镜像保存为tar文件：docker save -i -o
- 20.从tar镜像中载入镜像：docker load
- 21.将指定的同期保存为tar包：docker export
- 22.从tar文件创建镜像：docker import
- 23.查看某运行容器的进程：docker top sth
- 24.暂停/恢复某一容器的所有进程：docker pause/unpause
- 25.标记镜像并归入仓库：docker tag
- 26.将镜像推送到远程仓库，默认为docker hub：docker push
- 27.获取容器的运行输出日志：docker log
- 28.启动容器,在其中运行指定命令：docker run
>	-a stdin 指定标准输入输出内容类型，可选 STDIN/STDOUT/STDERR 三项；
	-d 后台运行容器，并返回容器ID；
	-i 以交互模式运行容器，通常与 -t 同时使用；
	-t 为容器重新分配一个伪输入终端，通常与 -i 同时使用；
	--name="nginx-lb" 为容器指定一个名称；
	--dns 8.8.8.8 指定容器使用的DNS服务器，默认和宿主一致；
	--dns-search example.com 指定容器DNS搜索域名，默认和宿主一致；
	-h "mars" 指定容器的hostname；
	-e username="ritchie" 设置环境变量；
	--env-file=[] 从指定文件读入环境变量；
	--cpuset="0-2" or --cpuset="0,1,2"
	绑定容器到指定CPU运行；
	-c 待完成
	-m 待完成
	--net="bridge" 指定容器的网络连接类型，支持 bridge /
	host / none
	container:<name|id> 四种类型；
	--link=[] 待完成
	--expose=[] 待完成  

