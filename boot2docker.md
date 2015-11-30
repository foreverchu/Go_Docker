### boot2docker

Mac下使用docker

---

*   brew install boot2docker  安装
*   boot2docker init 创建Docker运行所需要的虚拟机环境，只要执行一次
*   boot2docker start 启动Docker的虚拟机环境
*   boot2docker shellinit 查看Docker客户端的环境变量
*   boot2docker ssh
*   如果在执行docker命令的时候出现类似如下错误 dial unix /var/run/docker.sock: no such file or directory 是因为没有设置正确的环境变量导致的，执行命令 eval "$(boot2docker shellinit)" 重新设置环境变量即可。
*   查看容器开放了哪些端口，使用命令docker port
*   在Mac下，使用boot2docker的时候，访问127.0.0.1是不行的，因为docker的宿主机是boot2docker的虚拟机，因此需要使用虚拟机的ip访问boot2docker ip获取ip后访问。
*   要关闭boot2docker使用命令boot2docker stop。
