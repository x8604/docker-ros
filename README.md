# docker-ros
- Kéo image ROS Noetic từ Docker Hub: `docker pull osrf/ros:noetic`
- Kiểm tra danh sách các image: `docker images`
- Kiểm tra danh sách các container: `docker ps`
- Khởi tạo 1 container ROS Noetic: `docker run -it --rm osrf/ros:noetic`
  - `docker run`: khởi chạy 1 container từ 1 image
  - `-i`: chạy container ở chế độ tương tác
  - `-t`: tạo 1 terminal ảo để tương tác với container
  - `--rm`: xóa container ngay khi nó dừng hoạt động
- Chạy container kết nối với X server: `docker run -it --rm -e DISPLAY=host.docker.internal:0 -v /tmp/.X11-unix:/tmp/.X11-unix osrf/ros:noetic-desktop-full bash`
