# Análise de Admissões com CID Preenchido

Este projeto tem como objetivo analisar admissões hospitalares verificando a presença do campo “CID da Alta” (Código Internacional de Doenças) em bases de produção de diferentes hospitais.

O código lê bases de dados (Excel/CSV), faz tratamento e padronização, calcula indicadores de preenchimento do CID e exporta os resultados em formato Excel, permitindo acompanhar a qualidade do registro médico.

# Funcionalidades:

- Leitura automática de arquivos Excel (.xlsx, .xls) e CSV de múltiplos hospitais.

- Padronização e limpeza de colunas-chave: Cód. Paciente, Cód. Admissão, Ano, Mês, Médico, Hospital (renomeada a partir da coluna Unidade) e CID da Alta.

- Tratamento de duplicados e correção de IDs que vinham com .0 (ex.: 1234.0 → 1234).

- Filtragem de admissões com CID válido (exclui nulos e “SEM ALTA”).

- Cálculo do número e percentual de admissões com CID preenchido em 4 granularidades: AMH → Ano, Mês, Hospital, H → Hospital, AMHM → Ano, Mês, Hospital, Médico e HM → Hospital, Médico

- Exportação dos resultados para Excel, prontos para análise ou integração em relatórios.

# Estrutura do Projeto

- notebook.ipynb -> Notebook principal com todo o processamento.

- Entradas -> arquivos .xlsx ou .csv contendo as admissões hospitalares.

- Saídas -> arquivos .xlsx com os resultados agregados por hospital e granularidade.

# Indicadores Gerados:

- Total de Admissões.

- Total de Admissões com CIDs Preenchidos.

- % Admissões Com CID Preenchido.

- % Admissões Sem CID Preenchido.

# Tecnologias Utilizadas:

- Python 3

- Pandas -> manipulação de dados

- NumPy -> apoio matemático

- Dateutil -> tratamento de datas

- OpenPyXL -> exportação para Excel
