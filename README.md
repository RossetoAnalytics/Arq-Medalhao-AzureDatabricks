# Arq-Medalhao-AzureDatabricks

Projeto desenvolvido criando um ETL a partir de um host local do SQL Server, usando Azure e Databricks com a configuração real de um ambiente de produção. Este projeto faz uso de vários recursos da Azure, como o gerenciamento de permissões, Azure Data Lake Storage Gen2 (ADLS2), Azure Active Directory (AAD), conectores, Data Factory, Azure Synapse Analytics, conteúdos dinâmicos para Queries automáticas e o Key Vault para guardar segredos. Além de PySpark e SQL.

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
  <summary>Recursos</summary>

  ![resourcegroup](https://github.com/user-attachments/assets/00bc9775-accc-49cf-b0c3-7677963e2608)

</details>

<details>
  <summary>Pipeline Data Factory</summary>

![Pipeline ADF](https://github.com/user-attachments/assets/d92b56df-7554-490c-b2ec-54ee01ec7d67)

</details>

<details>
  <summary>Data Source</summary>

https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms

</details>
