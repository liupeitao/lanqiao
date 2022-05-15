## conda配置

1. #### download and install

    `https://www.anaconda.com/products/distribution#Downloads`

   ```shell
   wget https://repo.anaconda.com/archive/Anaconda3-2021.11-Linux-x86_64.sh
   
   sh Anaconda3-2021.11-Linux-x86_64.sh
   ```

   安装过程全部回答yes

2. #### environment configuration 

   ```shell
   sudo vim .bashrz
   
   export PATH=/home/liupeitao/anaconda3/bin:$PATH
   ```

3. 常用命令

   1. conda create -n {env_name} python={python_version}
   2. conda activate env_name