## Các bước chuẩn bị

1. Cài đặt Docker và Docker Swarm
2. Kiểm tra ngày giờ server
    ### Kiểm tra timezone
    $ ls -l /etc/localtime
    $ timedatectl

    ### Set timezone
    $ sudo timedatectl set-timezone Asia/Ho_Chi_Minh

3. Clone code
$ git clone https://github.com/mrchanvit/docker-traefik-portainer.git ./src

4. Thay domain trong file /home/tmc/src/core/docker-compose.yml
5. Thay email đăng ký free ssl tại /home/tmc/src/core/traefik-data/traefik.yml
6. Thay đổi user hệ thống tại /home/tmc/src/core/traefik-data/configurations/dynamic.yml
    Để tại user mới sử dụng lệnh 
    $ sudo apt install apache2-utils
    $ echo $(htpasswd -nb username matkhau)
7. Đổi quyền file acme.json sang 600
    $ sudo chmod 600 /path/src/core/traefik-data/acme.json
8. Chạy stack, thay sys bằng tên hệ thống (Tùy chọn)
$ cd src/core
$ docker stack deploy -c docker-compose.yml sys


