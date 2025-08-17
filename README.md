# TelecomXAlura

TelecomX ETL - Processamento de Dados de Telecomunicações
📌 Visão Geral

Este projeto realiza o Processamento ETL (Extração, Transformação e Carga) de dados de telecomunicações a partir de um arquivo JSON (TelecomX_Data.json).
O pipeline inclui:

Extração: Leitura de arquivos JSON e conversão para DataFrame.

Transformação: Limpeza, padronização, conversão de tipos e criação de colunas derivadas.

Carga e Análise: Salvamento em CSV e Parquet, geração de estatísticas descritivas.

Relatório e Visualizações: Criação de gráficos, análise de qualidade e relatório textual.

O projeto utiliza Python, pandas, Seaborn, Matplotlib e manipulação de datas.

🛠 Tecnologias Utilizadas

Python 3.10+

pandas

matplotlib

seaborn

json

datetime

os

📂 Estrutura de Pastas
TelecomX_ETL/
│
├─ TelecomX_Data.json       # Arquivo de dados brutos
├─ etl_telecomx.py          # Script principal ETL
├─ README.md                # Este documento
└─ output/                  # Pasta onde os resultados serão salvos
   ├─ TelecomX_Data_Tratado_TIMESTAMP.csv
   ├─ TelecomX_Data_Tratado_TIMESTAMP.parquet
   └─ relatorio_TIMESTAMP/
       ├─ distribucao_<coluna>.png
       ├─ top10_<coluna>.png
       ├─ pie_<coluna>.png
       ├─ tendencia_mensal.png
       └─ relatorio_qualidade.txt

⚙ Funcionalidades
1. Extração

Leitura de arquivos JSON com múltiplos formatos (lista ou dicionário).

Conversão automática para DataFrame do pandas.

Visualização inicial de registros e estrutura do DataFrame.

2. Transformação e Limpeza

Remoção de colunas irrelevantes.

Conversão de colunas para tipos adequados:

datetime (ex.: data, data_inicio)

numérico (ex.: valor, duracao)

categoria (ex.: plano, status)

texto (ex.: cliente, cidade)

Padronização de textos (maiúsculas e sem espaços extras).

Criação de colunas derivadas:

ano_mes: período mensal

dias_contrato: diferença entre data_fim e data_inicio

duracao_horas: duração em horas

3. Salvar e Analisar

Salvamento em CSV e Parquet na pasta output.

Estatísticas descritivas de colunas numéricas e categóricas.

Distribuição de registros por mês.

4. Relatório e Visualizações

Gráficos de distribuição para colunas numéricas.

Top 10 categorias e gráficos de pizza para colunas categóricas.

Tendência mensal de registros.

Relatório de qualidade com:

Valores nulos

Tipos de dados

Estatísticas descritivas

Todos os arquivos são salvos em pasta timestamp para rastreabilidade.

🚀 Como Executar

Clone este repositório:

git clone https://github.com/seu-usuario/TelecomX_ETL.git
cd TelecomX_ETL


Instale as dependências:

pip install pandas matplotlib seaborn


Execute o script ETL:

python etl_telecomx.py


Verifique a pasta output para arquivos tratados e relatório.

📊 Resultados Esperados

Arquivos CSV e Parquet com dados limpos e transformados.

Gráficos de distribuição e tendências mensais.

Relatório de qualidade detalhado em relatorio_qualidade.txt.

📝 Observações

Certifique-se de que o arquivo TelecomX_Data.json esteja na raiz do projeto.

O script cria pastas output automaticamente.

O ETL é tolerante a dados ausentes e tipos incorretos.
