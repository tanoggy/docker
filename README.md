
# Docker 
List mấy thứ vui vẻ
- [Image | GIF](#image--gif)
 - [Cách cài đặt Docker trên Ubuntu](#install-docker-ubuntu) 
 - 
 - 
#   [Cách cài đặt Docker trên Ubuntu](#install-docker-ubuntu) 

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
# Image | GIF
![myImage](https://media.giphy.com/media/XRB1uf2F9bGOA/giphy.gif)
    
    ![myImage](https://media.giphy.com/media/XRB1uf2F9bGOA/giphy.gif)
    
See more [Markdown Extras - Image Align](https://github.com/fefong/markdown_readme/blob/master/markdown-extras.md#image-align)    