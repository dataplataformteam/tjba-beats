## Coleta PostgreSql

### Configuração
O arquivo **metricbeat.yml** deve ser alterado apontando para o servidor do PostgreSql, conforme oirentação abaixo descrita:

**Alterar às seguintes linhas do arquivo**
  * 227 - Deve-se colocar o ip do servidor PostgreSql, o container deve ter acesso a está rede.
  * 230 - Colocar nome do usuário PostgreSql, com permissão de admin.
  * 233 - Colocar a senha do usuário utilizado.

### Build

```
docker-compose up -d
````
