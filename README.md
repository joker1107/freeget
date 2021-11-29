# 部署方法：
# 配置文件 /home/ubuntu/config.txt 


# 服务端执行 

wget https://github.com/joker1107/freeget.git

./van.v1.run server /home/ubuntu/config.txt

# 中转执行 （如使用无中转方式无需执行，使配置文件中 proxy 与server ip 一致）
./van.v1.run proxy /home/ubuntu/config.txt

#  客户端执行 
./van.v1.run client /home/ubuntu/config.txt

# 检验代理是否ok,
 curl -x socks5://127.0.0.1:1080 icanhazip.com
    
# 检测本机dns是否正确  
   ping asia2.ethermine.org
   #解析的地址为 172.65.239.73 说明dns ok

#  将客户端的ip设为网关 并将dns解析设为代理ip
