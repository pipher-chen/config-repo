# config-repo

## iovCloud-platform

易路拍&移动天后台代码


### 启动完成进行验证
启动完成打开 http://localhost:18070/swagger-ui.html#!

### mongodb相关
启动

在/usr/local/mongodb/bin下

mongod -f mongodb.conf 或 ./mongod -f mongodb.conf

关闭

mongod -f ./mongodb.conf --shutdown  或./mongod -f ./mongodb.conf --shutdown


#es相关
sh /home/es/elasticsearch-5.5.2/bin/elasticsearch -d

#mongo-connector相关
mongo-connector -m 192.168.15.3:27017 -t 192.168.15.3:9200 -d elastic2_doc_manager -a root -p 123456 -n db_iovcloud.*

nohup mongo-connector -m 192.168.15.3:27017 -t 192.168.15.3:9200 -d elastic2_doc_manager -a root -p 123456 -n db_iovcloud.* > /home/usedcar/mongo-connector.file 2>&1 & tail -f /home/usedcar/mongo-connector.file

ps -ef | grep mongo-connector

/root/mongo-connector.log


#elasticsearch-head
nohub npm run start &
