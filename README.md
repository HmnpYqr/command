# Command 常用命令大全

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
# 轻量级网络流量监控工具
vnstat
```

```bash
# 查看所有进程
ps aux
```

### Ubuntu 包管理器相关命令

```bash
# 更新软件包列表并升级所有已安装的软件包
sudo apt update && sudo apt upgrade -y
```

```bash
# 全部升级（包括自动删除不需要的包）
sudo apt full-upgrade
```

```bash
# 清理无用的安装包
sudo apt autoremove
```

### Ubuntu 服务管理命令

#### 启动/停止/重启服务

```bash
# 启动服务
sudo systemctl start [服务名]

# 停止服务
sudo systemctl stop [服务名]

# 重启服务
sudo systemctl restart [服务名]

# 重新加载配置（不重启服务）
sudo systemctl reload [服务名]
```

#### 查看服务状态

```bash
# 查看单个服务状态
systemctl status [服务名]

# 查看所有运行中的服务
systemctl list-units --type=service --state=running

# 查看失败的服务
systemctl --failed
```

#### 启用/禁用服务

```bash
# 启用服务（开机自启）
sudo systemctl enable [服务名]

# 禁用服务（取消开机自启）
sudo systemctl disable [服务名]

# 查看服务是否启用
systemctl is-enabled [服务名]
```

### Ubuntu 文件管理和文档编辑命令

#### 文件管理

```bash
# 移动或重命名文件/文件夹
mv <源路径> <目标路径>

# 显示目录中文件及其属性信息
ls

# 复制文件或目录
cp <源文件> <目标文件>
cp -r <源文件夹> <目标文件夹>

# 创建目录文件
mkdir <文件夹名>

# 显示当前工作目录的路径
pwd

# 压缩和解压缩文件
tar -czvf <压缩包名>.tar.gz <文件或目录>
tar -xzvf <压缩包名>.tar.gz

# 切换目录
cd <目录路径>

# 改变文件或目录权限
chmod <权限> <文件或目录>
```

#### 文档编辑

```bash
# 在终端设备上显示文件内容
cat <文件名>

# 强大的文本搜索工具
grep <关键字> <文件名>

# 删除文件或目录
rm <文件名>
rm -r <文件夹名>

# 输出字符串或变量值
echo "内容"
echo $变量

# 查看文件尾部内容
tail <文件名>

# 删除空目录文件
rmdir <空目录名>

# 批量编辑文本文件
sed 's/原内容/新内容/g' <文件名>

# 文本编辑器
vi <文件名>
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

```bash
# 临时使用清华大学镜像安装包
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple <包名>
```

```bash
# 临时使用清华大学镜像升级 pip
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pip -U
```

```bash
# 设置清华大学镜像为默认（pip >= 10.0.0）
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

## git 相关命令

### 仓库初始化与克隆

```bash
# 初始化 git 仓库
git init

# 克隆仓库
git clone <仓库地址>
```

### 文件操作与快照提交

```bash
# 查看当前状态
git status

# 添加文件到暂存区
git add <文件名>

# 添加当前目录下所有更改到暂存区
git add .

# 提交更改
git commit -m "提交说明"

# 比较暂存区和工作区的差异
git diff

# 使用外部差异工具查看文件更改
git difftool

# 比较两个提交范围之间的差异
git range-diff <commit1> <commit2>

# 回退版本
git reset <commit>

# 删除文件（从暂存区和工作区）
git rm <文件名>

# 移动或重命名工作区文件
git mv <源文件> <目标文件>

# 添加注释
git notes add -m "注释内容" <commit>
```

### 分支与切换

```bash
# 分支切换
git checkout <分支名>

# 使用 switch 切换分支（Git 2.23+）
git switch <分支名>

# 恢复或撤销文件的更改（Git 2.23+）
git restore <文件名>
```

### 查看对象与日志

```bash
# 显示 Git 对象的详细信息
git show <对象>

# 查看历史提交记录
git log

# 以列表形式查看指定文件的历史修改记录
git blame <文件名>

# 生成简洁的提交日志摘要
git shortlog

# 生成基于标签系统的可读字符串描述当前提交
git describe
```

### 远程操作

```bash
# 查看远程仓库
git remote -v

# 添加远程仓库
git remote add origin <远程仓库地址>

# 从远程获取代码库
git fetch

# 下载远程代码并合并
git pull

# 上传本地代码到远程仓库
git push

# 管理包含其他 Git 仓库的项目
git submodule
```

## Docker 命令

### 容器生命周期管理

```bash
# 创建并启动一个新容器
docker run <参数> <镜像名>

# 启动容器
docker start <容器名或ID>

# 停止容器
docker stop <容器名或ID>

# 重启容器
docker restart <容器名或ID>

# 立即终止一个或多个正在运行的容器
docker kill <容器名或ID>

# 删除一个或多个已经停止的容器
docker rm <容器名或ID>

# 暂停容器中的所有进程
docker pause <容器名或ID>

# 恢复被暂停的容器
docker unpause <容器名或ID>

# 创建但不启动容器
docker create <参数> <镜像名>

# 在运行中的容器内执行命令
docker exec -it <容器名或ID> <命令>

# 重命名容器
docker rename <旧容器名> <新容器名>
```

### 容器操作

```bash
# 列出所有容器
docker ps -a

# 获取容器详细信息
docker inspect <容器名或ID>

# 显示容器中的运行进程
docker top <容器名或ID>

# 附加到正在运行的容器
docker attach <容器名或ID>

# 获取 Docker 守护进程事件
docker events

# 查看容器日志
docker logs <容器名或ID>

# 等待容器停止并获取退出代码
docker wait <容器名或ID>

# 导出容器文件系统为 tar 归档
docker export <容器名或ID> -o <文件名>.tar

# 显示容器端口映射
docker port <容器名或ID>

# 实时显示容器资源使用情况
docker stats <容器名或ID>

# 更新容器资源限制
docker update --memory <大小> --cpus <数量> <容器名或ID>
```

### 容器 rootfs 操作

```bash
# 保存容器为新的镜像
docker commit <容器名或ID> <新镜像名>

# 容器与主机之间复制文件
docker cp <源路径> <目标路径>

# 显示容器文件系统变更
docker diff <容器名或ID>
```

### 镜像仓库操作

```bash
# 登录 Docker 仓库
docker login

# 登出 Docker 仓库
docker logout

# 拉取镜像
docker pull <镜像名>

# 推送镜像
docker push <镜像名>

# 搜索镜像
docker search <关键字>
```

### 本地镜像管理

```bash
# 列出本地镜像
docker images

# 删除镜像
docker rmi <镜像ID>

# 给镜像打标签
docker tag <镜像ID> <新标签>

# 从 Dockerfile 构建镜像
docker build -t <镜像名:标签> <Dockerfile目录>

# 查看镜像历史层信息
docker history <镜像名>

# 保存镜像到 tar 文件
docker save -o <文件名>.tar <镜像名>

# 从 tar 文件加载镜像
docker load -i <文件名>.tar

# 导入镜像
docker import <文件名>.tar
```

### 信息与版本

```bash
# 显示 Docker 系统信息
docker info

# 显示 Docker 版本信息
docker version
```

### Docker Compose 常用命令

```bash
# 构建服务
docker compose build

# 启动服务
docker compose up -d

# 停止服务
docker compose stop

# 重启服务
docker compose restart

# 查看服务状态
docker compose ps

# 删除服务
docker compose rm

# 列出所有 compose 项目
docker compose ls
```

### 网络相关命令

```bash
# 列出所有网络
docker network ls

# 创建新网络
docker network create <网络名>

# 删除网络
docker network rm <网络名>

# 连接容器到网络
docker network connect <网络名> <容器名或ID>

# 断开容器与网络连接
docker network disconnect <网络名> <容器名或ID>
```

### 卷相关命令

```bash
# 列出所有卷
docker volume ls

# 创建新卷
docker volume create <卷名>

# 删除卷
docker volume rm <卷名>

# 查看卷详细信息
docker volume inspect <卷名>
```

## screen 命令

```bash
# 创建名为 name 的会话
screen -S name

# 创建一个会话，系统自动命名
screen
```

```bash
# 退出当前 screen 会话（程序仍在后台执行）
# 按 Ctrl+a 后再按 d
Ctrl+a d
```

```bash
# 查看当前已有的 screen 会话
screen -ls
```

```bash
# 进入某个会话
screen -r <会话ID或名称>
```

### 窗口操作快捷键

- `Ctrl+a w`：展示当前会话中的所有窗口
- `Ctrl+a c`：创建新窗口
- `Ctrl+a n`：切换至下一个窗口
- `Ctrl+a p`：切换至上一个窗口
- `Ctrl+a <数字>`：切换至编号为数字的窗口
- `Ctrl+a k`：杀死当前窗口

```bash
# 删除某个会话
screen -S <your_screen_name> -X
