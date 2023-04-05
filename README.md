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
```

### Conjunto de métricas de instruções PostgreSQL

>⚠️ Habilitar este recurso aumentará o uso de memória do servidor.

Para habilitar a coleta de métricas de intruções deseve-se esecutar os seguintes comandos(terminal postgresql) abaixo para configurar às variáveis e criar a extension:

```
postgres=#  shared_preload_libraries = 'pg_stat_statements';
postgres=#  pg_stat_statements.max = 10000;
postgres=#  pg_stat_statements.track = all;
postgres=#  CREATE EXTENSION pg_stat_statements;
```

Como resultado algumas visualizações passaram a serem alimentadas com novas métricas.

![dashboard](https://github.com/dataplataformteam/tjba-beats/blob/main/dashboard.png)

[![Linkedin: Vectra](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&link=https://www.linkedin.com/in/houstonsantos/)](https://www.linkedin.com/company/vectra-cs/mycompany/) 

[**Vectra Consultoria e Serviços**](https://www.vectracs.com.br/home#/home)