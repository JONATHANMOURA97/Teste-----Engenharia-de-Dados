Claro, aqui está uma versão melhor formatada do readme:

---

# Projeto de Engenharia de Dados

## Descrição
Este projeto é uma demonstração de engenharia de dados, onde são apresentados diferentes tipos de arquivos e notebooks utilizados para criar e analisar conjuntos de dados de vendas.

## Estrutura do Projeto
- **Teste - Engenharia de dados (1).ipynb**: Notebook Jupyter contendo o código e a análise exploratória dos dados de vendas.
- **Teste - Engenharia de dados.html**: Uma versão HTML do notebook acima mencionado.
- **create_sales_dataset.ipynb**: Notebook Jupyter utilizado para criar o conjunto de dados de vendas.
- **sales_dataset.csv**: Conjunto de dados de vendas em formato CSV.
- **teste - Engenharia de Dados_JONATHAN MOURA.pdf**: Documento em PDF relacionado à engenharia de dados.

## Uso
- **Teste - Engenharia de dados (1).ipynb**: Execute este notebook para visualizar a análise dos dados de vendas.
- **create_sales_dataset.ipynb**: Utilize este notebook para criar conjuntos de dados de vendas.
- **sales_dataset.csv**: Conjunto de dados de vendas para análise.

## Contribuição
Contribuições são bem-vindas! Se você deseja contribuir com melhorias ou correções, por favor, abra uma issue ou envie uma solicitação de pull request.

## Autores
Este projeto foi desenvolvido por Jonathan Moura.

## Licença
Este projeto está licenciado sob a MIT License.

---

## Notebook Jupyter: Teste - Engenharia de dados.ipynb

### Descrição
Este notebook Jupyter demonstra um pipeline de processamento de dados utilizando o Apache Spark para análise e preparação de um conjunto de dados de vendas. Ele inclui etapas para carregar dados, limpar e transformar os dados, realizar análises estatísticas básicas e visualizar os resultados.

### Bibliotecas Utilizadas
- **pyspark.sql.SparkSession**: Para iniciar a sessão do Spark e carregar dados.
- **pyspark.sql.functions**: Para aplicar funções às colunas do DataFrame.
- **pyspark.sql.types**: Para definir e converter tipos de dados.
- **pyspark.ml.clustering.KMeans**: Para aplicar o algoritmo de clustering K-means aos dados.
- **pyspark.ml.feature.VectorAssembler**: Para transformar os recursos em um vetor para o modelo K-means.
- **matplotlib.pyplot**: Para visualização de gráficos.
- **seaborn**: Para visualização estatística.

### Funcionalidades
1. **Carregar Dados**: Utiliza o Spark para carregar um conjunto de dados de vendas em formato CSV.
2. **Limpeza e Transformação de Dados**:
   - Converte a coluna 'Date' para o tipo data.
   - Preenche valores nulos com 0.
   - Aplica regex simples na coluna 'Category' para corrigir possíveis erros.
   - Garante que as colunas 'Quantity' e 'Price' não contenham números negativos.
   - Ajusta os tipos de dados das colunas.
3. **Análise Estatística e Transformação de Dados**:
   - Calcula o valor total de cada transação.
   - Agrega os dados para obter estatísticas de vendas por produto e por categoria.
4. **Salva os Dados**:
   - Salva os dados transformados e agregados em formato Parquet.
   - Salva os mesmos dados em formato Delta Lake para aproveitar as funcionalidades adicionais.
5. **Modelagem de Clusters com K-means**:
   - Prepara os dados para o modelo K-means.
   - Treina o modelo e adiciona previsões de clusters aos dados.
   - Classifica os clientes em categorias com base na média de quantidade comprada.
6. **Visualização de Dados**:
   - Gera gráficos de barras mostrando o total de vendas por produto e por categoria.

### Utilização
- Execute o notebook em uma plataforma que suporte Apache Spark.
- Certifique-se de fornecer o caminho correto para o arquivo CSV de vendas.
- Siga as instruções passo a passo para carregar, limpar, transformar, analisar e visualizar os dados.

### Observações
- Este notebook foi criado para fins de demonstração e teste de processamento de dados utilizando o Apache Spark.
- Alguns caminhos de salvamento de arquivos estão especificados para o ambiente do Databricks, e podem precisar ser ajustados para o seu ambiente específico.

### Autor
Este notebook foi criado por JONATHAN MOURA.

### Licença
Este notebook está disponível sob a [MIT License](https://opensource.org/licenses/MIT).

---

## Notebook Jupyter: create_sales_dataset.ipynb

### Descrição
Este notebook Jupyter é responsável por gerar um conjunto de dados de vendas fictícias com informações incorretas para fins de demonstração e teste.

### Bibliotecas Utilizadas
- **pandas**: Para manipulação e análise de dados.
- **random**: Para gerar números aleatórios.
- **faker**: Para gerar dados fictícios de clientes.

### Funcionalidades
1. **Gerar Datas Aleatórias**: Utiliza a função `generate_random_dates()` para gerar datas de vendas aleatórias dentro de um intervalo específico.
2. **Gerar Dados de Vendas**: Cria um conjunto de dados de vendas com as seguintes informações:
   - Data da venda
   - Produto vendido
   - Categoria do produto
   - Quantidade vendida
   - Preço unitário
   - Total da venda
   - Nome do cliente
   - Região da venda
3. **Introduzir Inconsistências nos Dados**: Intencionalmente introduz algumas inconsistências nos dados, como preços negativos, quantidades negativas e categorias incorretas.
4. **Salvar o Conjunto de Dados**: Salva o DataFrame de vendas gerado como um arquivo CSV.

### Utilização
- Execute o notebook para gerar o conjunto de dados de vendas.
- O arquivo CSV resultante será salvo no caminho especificado no código.

### Observações
- Este conjunto de dados foi criado para fins de demonstração e teste, e contém 50% de dados incorretos ou inconsistentes, introduzidos de forma intencional para simular situações reais de limpeza e preparação de dados.

### Autor
Este notebook foi criado por JONATHAN MOURA.

### Licença
Este notebook está disponível sob a [MIT License](https://opensource.org/licenses/MIT).
