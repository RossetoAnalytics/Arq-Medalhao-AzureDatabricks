# PySpark Medalhão: Azure ETL Pipeline

Projeto desenvolvido criando um ETL a partir de um host local do SQL Server, usando Azure e Databricks em uma configuração de um ambiente de produção. Este projeto faz uso de vários recursos da Azure, como o gerenciamento de permissões, Azure Data Lake Storage Gen2 (ADLS2), Azure Active Directory (AAD), conectores, Data Factory, Azure Synapse Analytics, conteúdos dinâmicos para queries automáticas e dinâmicas, Key Vault para guardar segredos. Além de PySpark e SQL, o workspace do Databricks foi utilizado para criar transformações de dados em uma arquitetura medalhão, aproveitando as capacidades do PySpark para processamento e transformação em escala.

<details>
  <summary>Requisitos</summary>
  
- Configuração de Self-Hosted Runtime para conexão entre Azure Data Factory e SQL Server
- Configuração de Java Runtime para rodar arquivos .parquet
- Configuração de Managed Identity (MI) entre o Databricks, Data Factory e ADLS2 
- Autenticação via Azure Active Directory (AAD)
- Configuração do Networking, incluindo a abertura de portas específicas no firewall para acesso entre Azure e SQL Server.
- Controle de ACLs (Access Control Lists) e RBAC (Role-Based Access Control).
- Integração com o Key Vault: Garantir que o Databricks e o Data Factory estão corretamente configurados para acessar segredos armazenados no Key Vault. Isso envolve: Criação de políticas de acesso no Key Vault e uso de linked services no Data Factory para acessar o Key Vault.
- Configuração de mount Azure Data Lake Storage Gen2 container no Databricks usando autenticação via token. (notebook uploaded)

</details>


<details>
  <summary>Grupo de Recursos</summary>

 ![image](https://github.com/user-attachments/assets/6176cc7a-e5a3-4644-aa26-1fd87a8e7327)


</details>

<details>
  <summary>Pipeline Data Factory</summary>

![image](https://github.com/user-attachments/assets/2d175355-854f-4fff-bf53-f732df7e3cff)


Notas: Ingestão dinâmica conectada ao SQL server seguido de transformações em camadas usando PySpark no Databricks

</details>

<details>
  <summary>Data Source</summary>

https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms

</details>

![371883148-711fa6c8-4c8a-4eec-bb1f-c4f13e556c79](https://github.com/user-attachments/assets/5cfff45a-a71a-4c07-b1bd-6b8c07567424)


