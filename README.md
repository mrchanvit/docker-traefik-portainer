## Các bước chuẩn bị

1. Cài đặt Docker và Docker Swarm
2. Kiểm tra ngày giờ server
    ### Kiểm tra timezone
    $ ls -l /etc/localtime
    $ timedatectl

    ### Set timezone
    $ sudo timedatectl set-timezone Asia/Ho_Chi_Minh

3. Chạy stack
$ git clone https://github.com/mrchanvit/docker-traefik-portainer.git ./src
$ cd src/core
$ docker-compose up -d

4. Thay domain trong file /home/tmc/src/core/docker-compose.yml
5. Thay email đăng ký free ssl tại /home/tmc/src/core/traefik-data/traefik.yml
6. Thay đổi user hệ thống tại /home/tmc/src/core/traefik-data/configurations/dynamic.yml
    Để tại user mới sử dụng lệnh 
    $ sudo apt install apache2-utils
    $ echo $(htpasswd -nb username matkhau)


# docker-traefik-portainer
