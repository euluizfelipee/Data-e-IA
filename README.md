# Data-e-IA

### 1 - Objetivo: 

O objetivo deste projeto é implementar um pequeno data warehouse. Para isso, desenvolveremos um processo ETL utilizando Python que extrai dados de arquivos CSV existentes e os armazena em um banco de dados Postgres, seguindo o modelo dimensional. O diagrama abaixo ilustra os componentes que serão utilizados no projeto.

### 2 - Objetivos de Aprendizagem:


Você aplicará diversos conhecimentos e tecnologias para desenvolver um processo ETL com Python como ferramenta principal. O objetivo da atividade será coletar dados presentes em arquivos CSV (diretório de entrada) para realizar o carregamento de fatos e dimensões no data warehouse que você criará no servidor PostgreSQL.

#### Conhecimentos Envolvidos:
- Linguagem SQL
- Python
- Banco de dados relacional
- Modelagem dimensional e data warehouse
- Git
- Fundamentos de ETL

#### Etapa I - Compreender os Dados
O diretório de entrada contém 6 arquivos em formato CSV, que são:

- olist_products_dataset.csv
- olist_customers_dataset.csv
- olist_order_items_dataset.csv
- olist_order_payments_dataset.csv
- olist_orders_dataset.csv
- olist_order_reviews_dataset.csv

Esses arquivos fazem parte do Conjunto de Dados Públicos de E-Commerce Brasileiro da Olist, disponível no Kaggle. Abra cada um dos arquivos e acesse a página do Kaggle para entender como os dados se relacionam.

#### Etapa II - Definir seu Ambiente
Para construir seu ambiente, você precisará instalar o PostgreSQL em seu PC.
Instale as bibliotecas necessárias para o seu script ETL.
Instale o PostgreSQL localmente.
Execute o arquivo etl.py.

#### Etapa III - Definir seu Modelo Dimensional
Aqui você precisará desenvolver um modelo de dados dimensional que permita responder perguntas sobre vendas sob as perspectivas de:
Clientes
Produtos
Categoria do Produto
Estados
Data da compra
Hora da compra
Tipo de pagamento utilizado
Métricas importantes a serem consideradas em suas tabelas de fatos são a pontuação de avaliação do pedido, valor pago, número de parcelas do pagamento, preço do produto e custo de envio.

#### Etapa IV - Criar o Data Warehouse no Script etl.py
Uma vez que seu modelo de dados esteja definido, contendo os fatos e dimensões necessários, você deve adicionar a sequência de comandos DDL ao arquivo etl.py para criar as tabelas no banco de dados pb_dw no servidor PostgreSQL. Você pode usar a biblioteca psycopg2 para interagir com o PostgreSQL usando Python.

#### Etapa V -  Realizar os Carregamentos ETL no Script etl.py
Com suas tabelas do data warehouse devidamente criadas, agora é hora de construir os carregamentos ETL. Você precisará inserir os registros nas tabelas de fatos e dimensões utilizando os arquivos CSV. Todos os passos de carregamento devem ser adicionados ao script etl.py, de modo que, ao executá-lo, toda a estrutura do seu data warehouse seja criada, assim como os dados inseridos nas respectivas tabelas.
Dica: Você pode usar a biblioteca pandas ou polars para manipular os conjuntos de dados. Não se esqueça de seguir as melhores práticas de Python apresentadas ao longo dos cursos.

#### Resultados Esperados
Assim que você executar seu código no script etl.py, deverá ver os  registros extraídos dos arquivos CSV em suas tabelas de fatos e dimensões no PostgreSQL.
Dica: Exponha a porta 5432 do contêiner PostgreSQL para uma porta local em seu host. Assim, você pode usar ferramentas como Dbeaver para visualizar a estrutura e os dados do seu banco de dados.

#### Entregáveis
Em seu repositório do Github, adicione um diretório chamado projeto-i. Dentro deste diretório, adicione um arquivo chamado README.md com explicações sobre a solução do projeto. Além disso, inclua todos os arquivos utilizados na solução, exceto pelos arquivos CSV no diretório de entrad