# Command

服务器常用命令

## Ubuntu 命令

### Ubuntu 系统相关命令

```bash
# 重启系统
sudo reboot
```

### Ubuntu 常用命令

```bash
# 以树状结构显示进程
htop
```

```bash
# 查看所有进程
ps aux
```

### Ubuntu 包管理器相关命令

```bash
# 更新软件包列表
sudo apt update
```

```bash
# 升级已安装的软件包
sudo apt upgrade
```

```bash
# 全部升级（包括自动删除不需要的包）
sudo apt full-upgrade
```

```bash
# 清理无用的安装包
sudo apt autoremove
```

### Ubuntu 服务相关命令

```bash
# 查看服务状态
systemctl status <服务名>
```

```bash
# 启动服务
sudo systemctl start <服务名>
```

```bash
# 停止服务
sudo systemctl stop <服务名>
```

```bash
# 重启服务
sudo systemctl restart <服务名>
```

```bash
# 使服务开机自启
sudo systemctl enable <服务名>
```

```bash
# 取消服务开机自启
sudo systemctl disable <服务名>
```

```bash
# 查看所有服务
systemctl list-units
```

### Ubuntu 文件操作相关命令

```bash
# 查看当前目录文件
ls
```

```bash
# 查看详细信息
ls -l
```

```bash
# 切换目录
cd <目录路径>
```

```bash
# 创建文件夹
mkdir <文件夹名>
```

```bash
# 删除文件
rm <文件名>
```

```bash
# 删除文件夹及其内容
rm -r <文件夹名>
```

```bash
# 复制文件
cp <源文件> <目标文件>
```

```bash
# 复制文件夹及其内容
cp -r <源文件夹> <目标文件夹>
```

```bash
# 移动或重命名文件/文件夹
mv <源路径> <目标路径>
```

```bash
# 查看文件内容
cat <文件名>
```

```bash
# 编辑文件（使用 nano 编辑器）
nano <文件名>
```

## 查看文件实时内容相关命令

```bash
# 实时查看文件内容（如日志文件）
tail -f <文件名>
```

```bash
# 查看最近100条记录并实时跟踪内容
tail -n 100 -f <文件名>
```

## pip 相关命令

```bash
# 查看 pip 版本
pip --version
```

```bash
# 安装包
pip install <包名>
```

```bash
# 升级包
pip install --upgrade <包名>
```

```bash
# 卸载包
pip uninstall <包名>
```

```bash
# 查看已安装的包列表
pip list
```

```bash
# 导出已安装包到 requirements.txt
pip freeze > requirements.txt
```

```bash
# 根据 requirements.txt 安装所有依赖
pip install -r requirements.txt
```

## git 相关命令

```bash
# 初始化 git 仓库
git init
```

```bash
# 克隆仓库
git clone <仓库地址>
```

```bash
# 查看当前状态
git status
```

```bash
# 添加文件到暂存区
git add <文件名>
```

```bash
# 提交更改
git commit -m "提交说明"
```

```bash
# 推送到远程仓库
git push
```

```bash
# 拉取远程仓库更新
git pull
```

```bash
# 查看提交日志
git log
```

## Docker相关命令

```bash
# 查看所有容器
docker ps -a
```

```bash
# 启动容器
docker start <容器名或ID>
```

```bash
# 停止容器
docker stop <容器名或ID>
```

```bash
# 重启容器
docker restart <容器名或ID>
```

```bash
# 删除容器
docker rm <容器名或ID>
```

```bash
# 查看所有镜像
docker images
```

```bash
# 删除镜像
docker rmi <镜像ID>
```

```bash
# 构建镜像
docker build -t <镜像名:标签> <Dockerfile所在目录>
```

```bash
# 运行容器
docker run -d --name <容器名> <镜像名>
```

```bash
# 查看容器日志
docker logs <容器名或ID>
```

## screen相关命令

```bash
# 新建一个名为 mysession 的会话
screen -S mysession
```

```bash
# 列出所有会话
screen -ls
```

```bash
# 重新连接到名为 mysession 的会话
screen -r mysession
```

```bash
# 退出当前会话（不关闭会话，按下快捷键）
Ctrl+a d
```

```bash
# 关闭会话（在会话内输入）
exit
```
