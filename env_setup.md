
```bash
# 安裝 Miniconda
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init bash

# 安裝 Katoolin
sudo apt-get install git
sudo git clone https://github.com/LionSec/katoolin.git && cp katoolin/katoolin.py /usr/bin/katoolin
sudo chmod +x /usr/bin/katoolin

# 更改 shebang 以使用 Python 2
sudo bash
head -n 1 /usr/bin/katoolin
sudo apt-get install python2
sudo sed -i '1s|#!/usr/bin/python|#!/usr/bin/python2|' /usr/bin/katoolin

# 執行 Katoolin
sudo katoolin
```
