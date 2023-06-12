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
