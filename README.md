### install kubernetes by ansible
### 环境
1. 阿里云vpc专用网络环境，vps私有ip 192.168.0.0/16
2. linux centos 7.4 发行版,建议使用服务商镜像制作自定义镜像(yum update -y)
3. 仅支持linux 或 mac os 作为执行主机
4. 需修改host文件,填入阿里云各主机外网ip
5. 测试主机均为单网卡,如有需要可针对修改

### 配置参考
[k8s](https://jimmysong.io/kubernetes-handbook/)
[ansible cheat sheet](https://gist.github.com/andreicristianpetcu/b892338de279af9dac067891579cad7d)

### Todo
1. flanneld 的 网络类型问题 vxlan -> hostgw
2. 优化跟进 k8s 1.11 release

### 成功安装的软件版本信息
1. docker 1.13.1
2. flanneld 0.7.1
3. kubernetes 1.11
