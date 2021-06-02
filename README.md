# docker_test
参考苏洋大神博客学习docker里nginx的应用

## 目录说明
```
.
├── ccat
├── nginx-autoindex   (尚未完成）
│   ├── autoindex
│   │   ├── footer.html
│   │   └── header.html
│   ├── build.js
│   ├── build.sh
│   ├── docker-compose.yml
│   ├── favicon.png
│   ├── LICENSE
│   ├── logo.png
│   ├── mime.types
│   ├── nginx.conf
│   ├── preview.png
│   ├── public
│   ├── README.md
│   └── src
│       ├── scripts
│       │   ├── 1.timeago.min.js
│       │   └── 2.footer.js
│       ├── styles
│       │   └── style.css
│       └── templates
│           ├── footer.html
│           └── header.html
├── nginx-health
│   ├── create-self-ca.sh   自签名证书脚本
│   ├── default.conf
│   ├── docker-compose.yml
│   └── ssl
│       ├── lab.io.conf
│       ├── lab.io.crt
│       └── lab.io.key
├── nginx-qrcode     (尚未完成）
│   ├── docker-compose.yml
│   ├── Dockerfile
│   └── nginx.conf
├── prebuilt-nginx-modules  （三方模块高效构建）
│   ├── app
│   │   └── nginx-time-api
│   │       ├── build.sh
│   │       ├── docker-compose.yml
│   │       ├── Dockerfile
│   │       └── nginx.conf
│   ├── baseImage
│   │   ├── Dockerfile.alpine
│   │   └── Dockerfile.debian
│   ├── make-base.sh
│   ├── make-image.sh
│   ├── modules
│   │   ├── dynamic-upstream
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   ├── echo
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   ├── headers-more
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   ├── http-redis
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   ├── memc
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   ├── misc
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   ├── redis2
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   ├── srcache
│   │   │   ├── Dockerfile.alpine
│   │   │   └── Dockerfile.debian
│   │   └── waf
│   │       ├── Dockerfile.alpine
│   │       └── Dockerfile.debian
│   ├── push-image.sh
│   └── README.md
└── README.md

```



## 笔记
https://www.yuque.com/thinban/ql94rz/togk3l



