# Docker Compose Wordpress

## Installation
```bash
git clone https://github.com/serhiihonchar1992/docker-compose-wordpress
```
## Usage
```bash
docker-compose up
```
or

```bash
docker compose up
```

If you want to connect to a database using your IDE, DataGrip, or other tools,
You need to expose the ports of the database outside

```yaml
mysql:
  image: mysql:8.0
  volumes:
    - ./mysql_data:/var/lib/mysql
  restart: always
  ports:
    - 3006:3306
  environment:
    MYSQL_ROOT_PASSWORD: root
    MYSQL_DATABASE: wordpress
    MYSQL_USER: wordpress
    MYSQL_PASSWORD: wordpress
```