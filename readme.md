
//running mongo db container 

docker run -d \
-p 27017:27017 \
--name mongo \
--net mongo \
-e MONGO_INITDB_ROOT_USERNAME:admin \
-e MONGO_INITDB_ROOT_PASSWORD:root \
mongo

//running mon express container 

docker run -d \
-p 8081:8081
-e ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
-e ME_CONFIG_MONGODB_ADMINPASSWORD=root \
--name mongo-express \
-e ME_CONFIG_MONGODB_SERVER=mongo \
mongo-express