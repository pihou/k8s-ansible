### install kubernetes by ansible
### 环境
1. 阿里云vpc专用网络环境，vps私有ip 192.168.0.0/16
2. linux centos 7.4 发行版,建议使用服务商镜像制作自定义镜像(yum update -y)
3. 仅支持linux 或 mac os 作为执行主机
4. 需修改host文件,填入阿里云各主机外网ip(绑定弹性网卡)

### 配置参考
[k8s](https://jimmysong.io/kubernetes-handbook/)

### 安全问题,详情请查看k8s官方手册
1. api-server 应关闭8080 insecure port 非回环ip地址绑定
2. kubelet 应开启api接口访问权限认证，以及关闭 insecure port

### 需要修改的配置
1. flanneld 需要开启--ip-masq选项，否则pod无法和外界通信（默认应该是开启的）
2. docker 需要关闭--ip-masq选项，否则跨node的pod间通信，原ip将被隐藏
