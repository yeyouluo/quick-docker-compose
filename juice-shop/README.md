## OWASP Juice Shop（本地靶场）

启动：docker-compose up -d
停止：docker-compose stop / start
重置进度：docker-compose down 后删除 ./data/juiceshop.sqlite，再 up -d

Score Board 进度存在 ./data/juiceshop.sqlite，容器重建不丢。

注意：./data 里的静态文件（static/、*.ts 等）来自镜像，bind mount 不会自动复制；
若 ./data 被整体删除，需要重新执行：
  docker create --name tmp-js docker.1panel.live/bkimminich/juice-shop:latest
  docker cp tmp-js:/juice-shop/data/. ./data/
  docker rm tmp-js
