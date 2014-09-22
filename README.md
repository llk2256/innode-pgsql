#下载dockerfile
git clone https://github.com/llk2256/innode-pgsql.git
cd  innode-pgsql       
#创建innode-pgsql镜像
docker build -t innode-pgsql .
#运行innode-pgsql容器
docker run -d -p 5432:5432 --name innode-pgsql -e POSTGRESQL_USER=test -e POSTGRESQL_PASS=test -e POSTGRESQL_DB=test innode-pgsql
