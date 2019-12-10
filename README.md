
# Docker 
List mấy thứ vui vẻ

 - [ Cách cài đặt Docker trên Ubuntu](#cách-cài-đặt-docker-trên-ubuntu)

# Cách cài đặt Docker trên Ubuntu

Mình sẽ hướng dẫn các bạn cách đơn giản nhất để cài Docker và Docker Compose trên Ubuntu

### Update những package

Việc này sẽ update những package hiện tại đang có để tránh những lỗi không đáng có trong quá trình cài đặt

```bash
sudo apt update 
sudo apt upgrade
```
### Gỡ Docker cũ trên máy
Nếu chưa cài lần nào thì có thể bỏ qua bước này
```bash
sudo apt remove docker docker-engine docker.io
```

### Cài đặt Docker
Docker có sẵn trên repository mặc định của Ubuntu nên chỉ cần gõ lệnh như bên dưới là được
```bash
sudo apt install docker.io
```
Chờ nó chạy xíu là xong, nó có hỏi thì chọn Y 
### Kiểm tra cài đặt và một số tuỳ chỉnh
Kiểm tra Docker đã được cài đặt thành công chưa với lệnh
```bash
sudo docker --version
```
Để chạy Docker lên các bạn dùng lệnh
```bash
sudo systemctl start docker
```
Cài đặt để Docker khởi động cùng hệ thống
```bash
sudo systemctl enable docker
```

Để chắc chắn mọi thứ đã hoạt động ổn định hết thì các bạn chạy Hello-word của Docker bằng lệnh bên dưới
```bash
sudo docker run hello-world
```
Hiện kết quả như bên dưới là OK
```bash
Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```
### Chạy Docker với non-root
Nếu các bạn chạy máy server thì thông thường sẽ login bằng account root bên việt gõ lệnh docker không cần sudo nó vẫn chạy, còn các bạn chạy ở máy cá nhân thì vẫn phải sudo, mình sẽ hướng dẫn các bạn add user của mình vào để chạy docker không cần root
Khi chạy non-root thì các bạn có thể gặp phải lỗi như bên dưới
```bash
docker: Cannot connect to the Docker daemon. Is the docker daemon running on this host?.
See 'docker run --help'.
```
Chạy lệnh để thêm user group docker
```bash
sudo adduser <user-name> docker
#ví dụ
sudo addgroup --system docker
```
Nó sẽ trả về kết quả
```bash
Adding user `oggy-docker' to group `docker' ...
Adding user oggy-docker to group docker
Done.
```
Vậy là từ nay user của chúng ta có thể sử dụng Docker mà không cần thêm sudo hay password nữa



