# webSlam
web slam 
# 环境   
node version :  v14.17.6    
ubuntu : 18.04     
#  install     
（1）安装第三方库    
```
source emsdk/emsdk_env.sh    
 cd ./webSlam/src/libs/   
./build.sh  
```     
（2） 编译webSlam     

``` 
cd ./webSlam/src/slam   
 mkdir build/   
 cd build/    
 emcmake cmake ..    
 emmake make install  
```
(3)  example 
     i. 安装nodejs 第三方package  
     ```   
     cd ./AlvaAR/examples/   
     npm install    
     ```    
     ii. 使用OpenSSL生成开放的key.pem和cert.pem证书文件  
      ```    
       openssl genpkey -algorithm RSA -out key.pem
       openssl req -new -key key.pem -x509 -days 365 -out cert.pem

       ```   
