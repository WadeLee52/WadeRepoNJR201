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

# 用 pyenv 安裝 Python 3.8.10 版本 (它會把 Python 安裝到 ~/.pyenv/versions/ 目錄下)
pyenv install 3.8.10

# 設定全域（global）預設的 Python 版本為 3.8.10 (執行後 python 就會指向 ~/.pyenv/versions/3.8.10/bin/python)
pyenv global 3.8.10

# 設定目前資料夾的 Python 版本為 3.8.10 (pyenv 會在當前資料夾（這裡是 ~/WadeRepoNJR201/）寫入一個 .python-version 檔案，內容就是 3.8.10，)
# 從此以後，在這個資料夾或其子資料夾中執行 python 就會使用 3.8.10
# local > global 的優先權，所以這會覆蓋 pyenv global 的設定
pyenv local 3.8.10

# 在目前的 Python（也就是 pyenv 的 3.8.10）環境下安裝特定版本的 pipenv 工具
# pipenv 是一個用來管理虛擬環境和套件（依照 Pipfile）的工具
pip install pipenv ==2022.4.8

# 用指定的 Python 執行檔建立 pipenv 虛擬環境
# 叫 pipenv 使用 ~/.pyenv/versions/3.8.10/bin/python 這個 特定版本的 Python 在你當前的資料夾（例如 ~/WadeRepoNJR201/）中 建立一個新的虛擬環境
# 建立後會產生.venv/ 資料夾（或是放在其他地方，依照 pipenv 設定）、Pipfile 檔案、Pipfile.lock
pipenv --python ~/.pyenv/versions/3.8.10/bin/python

# 安裝Package
pipenv install flask==2.3.3

# 單純在當下環境使用Python
python

# 在虛擬的Python環境下使用Python
pipenv run python

# 為了省麻煩，直接將當下環境切換成虛擬環境
# 輸入 Ctrl+Shift+P，選擇你要的虛擬環境(直譯器)
# 再開啟新的Terminal

# 建立package
pipenv install -e .

