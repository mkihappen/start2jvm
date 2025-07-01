### 曾经多次尝试编译JDK均失败（主要是Windows环境）
### 再次通过WSL尝试，WSL/Ubuntu-24.04，失败 ---------- 环境问题（gcc、make版本问题，参见源码文件中的README）
### 使用Ubuntu-18.04，gcc-7.5，make-4.1，还需要加一个configure选项：--with-extra-cflags=-Wno-deprecated-declarations（不然出现“readdir64_r”相关错误会编译失败）
#### 参考
- sudo apt-get install -y build-essential
- sudo apt-get install -y libfreetype6-dev
- sudo apt-get install -y libcups2-dev
- sudo apt-get install -y libx11-dev libxext-dev libxrender-dev libxrandr-dev libxtst-dev libxt-dev
- sudo apt-get install -y libasound2-dev
- sudo apt-get install -y libffi-dev
- sudo apt-get install -y autoconf
- sudo apt-get install -y libfontconfig1-dev
- sudo apt-get install openjdk-11-jdk
- #### bash configure --enable-debug --with-jvm-variants=server --with-extra-cflags=-Wno-deprecated-declarations
- #### make images
- #### make install

##### 编译版本：JDK11-27，BOOT JDK也是11
