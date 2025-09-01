# banco-de-dados-azure.
# Desafio de Projeto: Criando um Banco de Dados SQL no Azure

Repositório criado para o Desafio de Projeto da [Digital Innovation One](https://dio.me). O objetivo é servir como um material de apoio, com resumos, anotações e a descrição do processo de criação de uma instância de Banco de Dados SQL na Microsoft Azure.

## 📝 Descrição do Desafio

O desafio consiste em praticar a configuração de um Banco de Dados SQL no Azure, documentando o processo e consolidando o conhecimento em um repositório que funcione como um guia de estudos sobre o tema.

---

## 🧠 Conceitos Fundamentais sobre o Banco de Dados SQL do Azure

### O que é o Banco de Dados SQL do Azure?
O Banco de Dados SQL do Azure é um serviço de banco de dados relacional inteligente e totalmente gerenciado (PaaS - Plataforma como Serviço). Ele automatiza tarefas como atualizações, provisionamento e backups, permitindo que os desenvolvedores foquem na aplicação.

### Modelos de Serviço (DTU vs. vCore)
-   **DTU (Unidade de Transação de Banco de Dados):** É um modelo mais simples, que combina recursos de computação (CPU), memória e E/S (leitura/gravação) em uma única unidade. Ideal para iniciantes e cargas de trabalho com demandas previsíveis.
-   **vCore (Núcleo Virtual):** Oferece maior flexibilidade, permitindo escalar os recursos de computação e armazenamento de forma independente. É o modelo recomendado para a maioria das cargas de trabalho de produção.

### Servidor Lógico (Logical Server)
No Azure, um banco de dados SQL reside dentro de um "servidor lógico", que atua como um ponto de administração central para um grupo de bancos de dados. Ele gerencia logins, regras de firewall e configurações que são compartilhadas por todos os bancos de dados dentro dele.

---

## 📄 Descrição do Processo de Criação

O processo para configurar uma instância do Banco de Dados SQL no Azure envolve as seguintes etapas:

### 1. Criação do Grupo de Recursos
Como boa prática, o primeiro passo é a criação de um **Grupo de Recursos**. Ele funciona como um contêiner para organizar todos os recursos relacionados ao projeto, facilitando o gerenciamento e o controle de custos.

### 2. Criação do Servidor SQL Lógico
Em seguida, é criado o Servidor Lógico que hospedará o banco de dados. Nesta etapa, define-se um nome de servidor globalmente exclusivo, as credenciais de administrador (login e senha) e a região onde o servidor será hospedado.

### 3. Configuração do Banco de Dados
Com o servidor configurado, o próximo passo é a criação do banco de dados em si. É preciso definir um nome para o banco e escolher o modelo de computação (como DTU ou vCore), selecionando o nível de desempenho e a capacidade de armazenamento adequados para a necessidade do projeto.

### 4. Configuração do Firewall
Uma etapa crítica para a segurança e o acesso é a configuração das regras de firewall do servidor. É fundamental habilitar a opção que permite o acesso de outros serviços do Azure e adicionar uma regra específica para o endereço IP do cliente, garantindo o acesso para fins de administração e desenvolvimento.

---

## 💡 Dicas e Boas Práticas

> **Segurança é Prioridade:** Sempre configure as regras de firewall para o **mínimo acesso necessário**. Evite liberar faixas de IP muito amplas (como 0.0.0.0).

> **Gerenciamento de Custos:** Para ambientes de estudo e desenvolvimento, utilize os modelos de serviço mais básicos (como o DTU Básico ou vCore sem servidor) para evitar custos inesperados. Use os **Alertas de Custo** do Azure.

> **Nomenclatura:** Adote um padrão de nomenclatura claro para seus recursos (ex: `rg-` para Grupo de Recursos, `sqlserver-` para Servidor, `sqldb-` para Banco de Dados). Isso facilita muito a gestão em projetos maiores.

## ✅ Conclusão

Este desafio prático foi excelente para consolidar o passo a passo da criação de um dos serviços PaaS mais populares do Azure. A documentação em formato de guia de estudos ajuda a fixar os conceitos e serve como um ótimo material para consultas futuras.
