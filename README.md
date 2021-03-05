## Các bước chuẩn bị

1. Cài đặt Docker và Docker Swarm
2. Kiểm tra ngày giờ server
    # Kiểm tra timezone
    $ ls -l /etc/localtime
    $ timedatectl

    # Set timezone
    $ sudo timedatectl set-timezone Asia/Ho_Chi_Minh

3. Thay domain trong file /home/tmc/src/core/docker-compose.yml
4. Thay email đăng ký free ssl tại /home/tmc/src/core/traefik-data/traefik.yml
5. Thay đổi user hệ thống tại /home/tmc/src/core/traefik-data/configurations/dynamic.yml
    Để tại user mới sử dụng lệnh 
    $ sudo apt install apache2-utils
    $ echo $(htpasswd -nb username matkhau)

## Chạy stack
```
$ git clone https://github.com/rafrasenberg/docker-traefik-portainer ./src
$ cd src/core
$ docker-compose up -d
```
# docker-traefik-portainer
