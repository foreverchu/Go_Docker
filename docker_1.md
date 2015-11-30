docker images

docker ps | docker ps -a


docker run -v /Users/xuhang:/mnt -it Images:tag  打开一个容器，并挂载/Users/xuhang 到/mnt


docker commit -m "update" -a "xuhang" ContainerId Image:tag 创建镜像

docker start ContainerId 启动暂停的容器
docker attach ContainerId  进入容器
exit | control +D 退出容器





