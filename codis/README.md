### Codis
本环境中每一个codis节点都有两个文件，一个是.yaml结尾，另一个是.yaml.bak结尾   
- yaml文件是采用在docker镜像中[codis-*-admin.sh](https://github.com/dlwangzg/dingxin-docker-image/blob/master/codis/codis-dashboard/target/admin/codis-dashboard-admin.sh)启动codis节点  
- yaml.bak文件是参考链接，在k8s command形式进行的
- 本环境中codis-dashboard-admin.sh的停止处理有问题，采用的是kill -9 $(cat "$CODIS_DASHBOARD_PID_FILE")，导致重启时报错,需修改该处理方式，或结合.bak处理方法，增加poststop处理   
出错信息如下
```
codis node already exists
```

