### Docker
Construção da imagem e inicialização

```bash
docker build -t playlistify-db .
docker run -d -p 3306:3306 --name=playlistify-mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=playlistify_database playlistify-db
```