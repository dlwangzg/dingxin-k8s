## Nginx使用
### 场景
本环境中nginx做为静态web服务器，同时也做为代理服务器使用
### 说明 
- dingxin_web.conf配置文件直接放到/etc/nginx/conf.d/目录下
- k8s nginx ingress不适用于此场景
- 若想使用k8s nginx ingress需要将动、静部分完全拆除方可
