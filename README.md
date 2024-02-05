### Docker
Construção da imagem e inicialização

```bash
docker build -t playlistify-db .
docker run -d -p 3306:3306 --name=playlistify-mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=playlistify_database playlistify-db
```


### Startup Projeto

```bash
# Migra as tabelas do banco de dados
python3 manage.py migrate

# Cria o usuario administrador
python3 manage.py createsuperuser
```

## Models Django
Ao criar algum model para a aplicação, deve-se atualizar as migrations com os seguintes comandos:

```bash
# Atualiza as migrações de acordo com as alterações dos models
python3 manage.py makemigrations

# Migra o banco de dados
python3 manage.py migrate
```