# Teste para contratação de Engenheiro de Dados

Realize um `fork` e suba o código desenvolvido dentro deste repositório.
- Disponibilizar o código desenvolvido via GitHub (realize um `fork` deste repositório) para avaliação. 
- Para comunicação, caso não tenha recebido algum contato, notifique rh@targetsoftware.com.br sobre a finalização do teste com o link do repositório.

### O que será avaliado:
  - Padrão utilizado de desenvolvimento;
  - Boas práticas aplicadas;
  - Aplicação de conceitos de performance;
  - Organização e desenho do processo de ETL.

### Diferenciais
  - Documentação
  - Organização
  - Modelagem e padrões
  - Lógica aplicada

### Origem
- Para a construção utilize o arquivo no repositório como base de dados de origem
- `base_atendimentos_simulada.txt`
----------------------------------------------------------

# 🧪 Desafio Power BI

## Objetivo
Criar um dashboard para análise de atendimentos e desempenho dos especialistas de cobrança, utilizando a base fornecida.

## Base de Dados
- Arquivo: `base_atendimentos_simulada.txt`
- Delimitador: Tabulação (`\t`)

## Tarefas
1. Importar o arquivo `.txt` no Power BI.
2. Realizar transformações necessárias:
   - Conversão de tipos (data, numéricos)
   - Limpeza de dados, se necessário
3. Criar medidas DAX para:
   - Total de Atendimentos
   - Valor total em cobrança
   - Média de duração dos atendimentos por especialista
   - % de atendimentos resolvidos
4. Criar visualizações:
   - Evolução de atendimentos por mês
   - Mapa com atendimentos por UF
   - Tabela com ranking dos 10 especialistas com maior valor cobrado
   - Gráfico de pizza por canal de atendimento
5. Criar filtros interativos por:
   - Categoria de Atendimento
   - UF

## Entregáveis
- Arquivo `.pbix` com a solução
- Duas screenshots do dashboard final (PNG ou JPEG)

----------------------------------------------------------

# 🧪 Desafio SAS

## Objetivo
Realizar análise estatística e tratamento de dados com SAS utilizando a base simulada de atendimentos.

## Base de Dados
- Arquivo: `base_atendimentos_simulada.txt`
- Local: `data/raw/base_atendimentos_simulada.txt`
- Delimitador: Tabulação (`\t`)

## Tarefas
1. Importar o arquivo no SAS utilizando `PROC IMPORT` ou `DATA step`.
2. Tratar os dados:
   - Conversão correta de datas
   - Tratamento de valores nulos (simule valores ausentes, se necessário)
3. Análises solicitadas:
   - Média, mediana e desvio padrão do valor em cobrança por UF
   - Distribuição da duração dos atendimentos
   - Percentual de cada situação de atendimento por canal
4. Segmentação:
   - Criar segmentação dos clientes com base no valor total em cobrança:
     - Baixo valor (< 1.000)
     - Médio valor (1.000 - 3.000)
     - Alto valor (> 3.000)

## Entregáveis
- Código `.sas` com comentários

----------------------------------------------------------
# 🧪 Desafio Databricks

## Objetivo
Manipular e transformar dados de atendimentos com Spark usando Databricks.

## Base de Dados
- Arquivo: `base_atendimentos_simulada.txt`
- Delimitador: Tabulação (`\t`)

## Tarefas
1. Subir o arquivo para o Databricks.
2. Ler o arquivo com Spark:
3. Criar uma **tabela Bronze** com os dados originais.
4. Criar uma **tabela Silver** com:
   - Conversão correta dos tipos de dados
   - Cálculo do tempo médio por especialista
   - Flag `Fechou_Acordo` (quando Situação = 'Resolvido' e Categoria = 'Acordo Fechado')
5. Criar uma **tabela Gold** agregada com:
   - Total de atendimentos
   - Valor médio em cobrança
   - % de acordos fechados por UF e mês
   - Salvar como Delta Table

## Entregáveis
- Link do notebook Databricks (compartilhável) ou arquivo `.dbc` exportado
