# WadeRepoNJR201
WadeRepoNJR201

#  查看所有 container（含已停止的）
docker ps -a

# 查看所有 image
docker images

#  停止單一 container
docker stop <container_id_or_name>


# 停止所有 container
docker stop $(docker ps -aq)

# 刪除單一 container
docker rm <container_id_or_name>

# 刪除所有已停止的 container
docker container prune -f

# 強制刪除所有 container
docker rm -f $(docker ps -aq)

# 刪除單一 image
docker rmi <image_id_or_name>

# 刪除所有 image
docker rmi -f $(docker images -aq)
