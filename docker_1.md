docker images

docker ps | docker ps -a


docker run -v /Users/xuhang:/mnt -it Images:tag  打开一个容器，并挂载/Users/xuhang 到/mnt


docker commit -m "update" -a "xuhang" ContainerId Image:tag 创建镜像

docker start ContainerId 启动暂停的容器
docker attach ContainerId  进入容器
exit | control +D 退出容器


docker search ubuntu|mysql 搜索镜像
docker pull ImageId 下载镜像



---


### 数据卷

数据卷是一个可供一个或多个容器使用的特殊目录，它绕过 UFS，可以提供很多有用的特性：

*   数据卷可以在容器之间共享和重用
*   对数据卷的修改会立马生效
*   对数据卷的更新，不会影响镜像
*   卷会一直存在，直到没有容器使用

数据卷的使用，类似于 Linux 下对目录或文件进行 mount。
