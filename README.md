# Projeto CoderHouse

Este projeto utiliza Jupyter Notebooks para coletar e processar dados de estados, municípios e bancos no Brasil, a partir de APIs públicas, e envia alertas para notificar o sucesso ou falha nas operações.

## Descrição

O código realiza as seguintes operações:
- **Busca dados de estados** a partir da API do IBGE usando o endpoint `/uf/v1`.
- **Busca dados de municípios** para cada estado retornado, a partir do endpoint `/municipios/v1/{sigla_estado}`.
- **Busca dados de bancos** utilizando o endpoint `/banks/v1`.
- Processamento e transformação dos dados em DataFrames do Pandas para facilitar a manipulação e a análise.
- Envia notificações para alertar sobre o status do processo utilizando a biblioteca `plyer`.

## Funcionalidades

- **Coleta de dados**: Através de requisições HTTP, o código coleta informações detalhadas sobre estados, municípios e bancos do Brasil.
- **Processamento de dados**: Os dados coletados são processados e estruturados em DataFrames para fácil manipulação e análise.
- **Notificações**: Utilizando a biblioteca `plyer`, o código envia notificações sobre o andamento do processo de coleta e processamento de dados.
  
## Dependências

- **requests**: Para fazer requisições HTTP aos endpoints de API.
- **pandas**: Para manipulação e análise de dados.
- **plyer**: Para exibir notificações de alerta no sistema operacional.

Instale as dependências usando o `pip`:

- /venv/Scripts/activate - Utilize o comando para ativar seu ambiente virtual

```bash
pip install pandas
pip install requests
pip install plyer
pip install sqlite3
python -m pip install -r requirements.txt
