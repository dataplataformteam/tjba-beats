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

[![Linkedin: Vectra](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&link=https://www.linkedin.com/in/houstonsantos/)](https://www.linkedin.com/company/vectra-cs/mycompany/) [**Vectra Consultoria e Serviços**](https://www.vectracs.com.br/home#/home)