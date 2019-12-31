#docker_MYSQL

Server에 처음 MySQL을 설치할 때 직접 apt-get을 이용햇 설치하는 방법도 있지만, docker를 이용하면 간편하다.

##Pre-requisite
* git clone https://github.com/mdsung/docker_MYSQL.git
* .env file

##.env file
echo -e "MYSQL_ROOT_PASSWORD=\nMYSQL_PASSWORD=\nMYSQL_USER=" > .env 로 생성한다. rootpassword, password, user에 각자 원하는 항목을 넣는다.

참고로 접속 port는 13306으로 되어 있다.

##docker-compose

docker-compose up -d

실행시키면 mysql의 도커가 실행된ㄷ.

##docker로 mysql 접속방법

* in local host: docker exec -it mysql mysql -u <user_id> -p 
* 원격 접속시: mysql -h --port -u <user_id> -p
