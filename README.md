<div align="center">

# Databricks Lakehouse Data Engineering Project

Modern **Data Engineering project** built with **Databricks, Apache Spark and Delta Lake**, demonstrating a full **Lakehouse architecture** with ingestion, batch & streaming pipelines, governance and Medallion layers.

<br>

<img src="https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white"/>
<img src="https://img.shields.io/badge/Apache%20Spark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white"/>
<img src="https://img.shields.io/badge/Delta%20Lake-0A84FF?style=for-the-badge"/>
<img src="https://img.shields.io/badge/PySpark-FF6F00?style=for-the-badge&logo=apache-spark&logoColor=white"/>

<br>

<img src="https://img.shields.io/badge/Unity%20Catalog-9333EA?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Delta%20Live%20Tables-10B981?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Lakehouse%20Architecture-Medallion-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Status-Complete-success?style=for-the-badge"/>

</div>

---

## Visão Geral

Este projeto demonstra a construção de uma **plataforma moderna de engenharia de dados utilizando Databricks e Apache Spark**, seguindo as melhores práticas da arquitetura **Lakehouse**.

O pipeline cobre todo o ciclo de vida dos dados:

• Ingestão de múltiplas fontes  
• Processamento distribuído com Spark  
• Armazenamento otimizado com Delta Lake  
• Pipelines automatizados  
• Streaming com Auto Loader  
• Governança e segurança com Unity Catalog  

O objetivo é simular um **ambiente de dados corporativo**, mostrando como construir pipelines escaláveis e confiáveis em uma plataforma Lakehouse.

---

## Arquitetura Lakehouse

O projeto segue a arquitetura **Medallion Architecture**, amplamente utilizada no Databricks.

<p align="center">

![Layer](https://img.shields.io/badge/Bronze-Raw%20Data-CD7F32?style=for-the-badge) 
→ 
![Layer](https://img.shields.io/badge/Silver-Cleaned%20Data-C0C0C0?style=for-the-badge) 
→ 
![Layer](https://img.shields.io/badge/Gold-Business%20Ready-FFD700?style=for-the-badge)

</p>

### Bronze Layer
Armazena os **dados brutos ingeridos das fontes originais**, sem transformações significativas.

Exemplos de ingestão:
- JSON
- CSV
- Imagens
- JDBC
- Streaming com Auto Loader

### Silver Layer
Camada responsável por **limpeza, padronização e enriquecimento dos dados**.

Inclui:
- Data cleaning
- Normalização
- Joins
- Transformações
- Data quality

### Gold Layer
Contém **dados prontos para análise e consumo por dashboards, BI e analytics**.

Inclui:
- Aggregations
- Business metrics
- Data marts

---

## Tecnologias Utilizadas

<p align="center">

<img src="https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white"/>
<img src="https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apache-spark&logoColor=white"/>
<img src="https://img.shields.io/badge/Delta%20Lake-0A84FF?style=flat"/>
<img src="https://img.shields.io/badge/PySpark-FF6F00?style=flat&logo=apache-spark&logoColor=white"/>
<img src="https://img.shields.io/badge/SQL-336791?style=flat"/>
<img src="https://img.shields.io/badge/Unity%20Catalog-9333EA?style=flat"/>
<img src="https://img.shields.io/badge/Delta%20Live%20Tables-10B981?style=flat"/>

</p>

Principais tecnologias utilizadas no projeto:

• **Databricks** — plataforma unificada para engenharia e análise de dados  
• **Apache Spark** — processamento distribuído em larga escala  
• **Delta Lake** — armazenamento confiável com ACID transactions  
• **PySpark** — transformação de dados distribuída  
• **Databricks SQL** — consultas analíticas  
• **Unity Catalog** — governança e controle de acesso  
• **Delta Live Tables** — pipelines declarativos

---

## Estrutura do Projeto

```
databricks-lakehouse-data-engineering/
│
├── dea01-databricks-lakehouse-platform
│   Introdução ao ambiente Databricks
│   Utilitários, magic commands e debugging
│
├── dea02-unity-catalog
│   Configuração do Unity Catalog
│   Controle de acesso e integração com cloud storage
│
├── dea03-etl-with-apache-spark
│   Pipelines ETL com Apache Spark
│
├── dea04-delta-lake
│   Funcionalidades avançadas do Delta Lake
│
├── dea05-databricks-jobs
│   Orquestração de pipelines Bronze, Silver e Gold
│
├── dea06-delta-live-tables
│   Pipelines declarativos com Delta Live Tables
│
├── dea07-databricks-sql
│   Consultas analíticas e exploração de dados
│
├── dea08-data-security
│   Governança e segurança de dados
│
└── README.md
```

---

## ETL com Apache Spark

O projeto inclui pipelines completos de **Extração, Transformação e Carga (ETL)** utilizando Spark.

Principais operações implementadas:

• Ingestão de dados de múltiplos formatos (CSV, JSON, Images, JDBC)  
• Data profiling  
• Transformações com PySpark  
• Joins e agregações  
• User Defined Functions (UDF)  
• Higher Order Functions  
• Streaming ingestion com Auto Loader  

Esses pipelines demonstram como processar **grandes volumes de dados de forma distribuída**.

---

## Delta Lake

O projeto utiliza **Delta Lake** para garantir confiabilidade e performance no armazenamento de dados.

Funcionalidades implementadas:

• **Transaction Log** para controle de versões  
• **Time Travel** para consultar versões anteriores de dados  
• **MERGE (Upsert)** para atualizações incrementais  
• **Insert Overwrite**  
• **OPTIMIZE** para compactação de arquivos  
• **ZORDER** para melhoria de performance em queries  
• **VACUUM** para limpeza de dados antigos  

Esses recursos permitem construir **data lakes confiáveis e performáticos**.

---

## Streaming com Auto Loader

O projeto demonstra ingestão de dados em **tempo quase real** utilizando Auto Loader.

Benefícios:

• Detecção automática de novos arquivos  
• Escalabilidade para grandes volumes de dados  
• Integração nativa com Delta Lake  
• Simplificação de pipelines de streaming

---

## Delta Live Tables

Também foram implementados pipelines usando **Delta Live Tables (DLT)**.

O DLT permite criar pipelines de forma **declarativa**, com:

• Monitoramento automático  
• Data quality checks  
• Lineage de dados  
• Pipelines gerenciados

Exemplo de pipelines implementados:

• Customers pipeline  
• Address pipeline  
• Orders pipeline

---

## Governança e Segurança

O projeto utiliza **Unity Catalog** para implementar governança centralizada.

Recursos utilizados:

• **Dynamic Views** para controle de acesso baseado em contexto  
• **Row Filters** para restringir acesso a linhas específicas  
• **Column Masks** para mascaramento de dados sensíveis  
• **ABAC (Attribute-Based Access Control)** com governed tags  

Esses mecanismos permitem aplicar **políticas de segurança e compliance em nível de dados**.

---

## Principais Funcionalidades

• Arquitetura Lakehouse completa  
• Pipelines Bronze, Silver e Gold  
• Processamento batch e streaming  
• Transformações distribuídas com PySpark  
• Governança com Unity Catalog  
• Otimizações com Delta Lake  
• Orquestração com Databricks Jobs  
• Pipelines declarativos com Delta Live Tables  

---

## Possíveis Extensões

O projeto pode ser expandido com:

- Integração com ferramentas de BI (Power BI, Tableau)
- Monitoramento de pipelines
- CI/CD para notebooks
- Data quality frameworks
- Integração com ML pipelines

---

## Autor

**Henrique Mourão**

<p align="center">
  <a href="https://github.com/Henrique-Mourao">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
  <a href="https://linkedin.com/in/henrique-mourão">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:henriquegamour4@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

---

<p align="center">
Projeto desenvolvido para fins educacionais e demonstração de habilidades em Data Engineering.
</p>
