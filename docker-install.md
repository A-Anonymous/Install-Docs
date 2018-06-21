# docker安装

标签： 安装教程

---

## **基本安装和启动docker**

    #yum update -y
    #yum -y install docker 
    #systemctl enable docker 
    #systemctl start docker


## **最新版或特定版安装和启动docker**

#### **配置docker阿里云yum源**
直接运行下面命令

    #cat >>/etc/yum.repos.d/docker.repo<<EOF
    [docker-ce-edge]
    name=Docker CE Edge - \$basearch
    baseurl=https://mirrors.aliyun.com/docker-ce/linux/centos/7/\$basearch/edge
    enabled=1
    gpgcheck=1
    gpgkey=https://mirrors.aliyun.com/docker-ce/linux/centos/gpg
    EOF

安装最新版docker ce版（社区免费版）

    #yum -y install docker-ce
    
### **特定版本安装**  
**查看docker-ce版本**

    #yum list docker-ce  --showduplicates |sort -r
**安装命令**

    #yum -y install docker-ce-<version>

    
### **查看docker版本**

    #docker --version  

### **启动docker**

    #systemctl enable docker
    #systemctl start docker 
    


   