# challenge2-data-science-telecom_x

# Análise de Evasão de Clientes (Churn)

## Visão Geral
Este projeto realiza uma análise completa dos fatores associados à evasão de clientes (churn) em uma empresa de telecomunicações, seguindo um fluxo de trabalho que vai desde a extração e transformação dos dados até a análise visual e recomendações estratégicas.

## Estrutura do Projeto
- `dados_processados.csv` - Dataset processado após ETL
- `analyze_data.py` - Script para análise inicial dos dados
- `generate_plots.py` - Script para geração de visualizações
- `graficos_proporcao_evasao.png` - Visualizações consolidadas
- `relatorio_analise_churn_atualizado.pdf` - Relatório final com análises e recomendações

## Fluxo de Trabalho Completo

### 1. Extração de Dados
- Carregamento direto dos dados brutos a partir de um arquivo JSON via URL
- Fonte de dados: TelecomX_Data.json da plataforma GitHub

### 2. Transformação de Dados
- Expansão das colunas com dicionários aninhados (customer, phone, internet, account)
- Separação da coluna 'Charges' em 'Monthly' e 'Total'
- Renomeação de todas as colunas para português
- Tradução dos valores categóricos (ex: 'Male'/'Female' para 'Masculino'/'Feminino')
- Preparação da coluna numérica de evasão para análise

### 3. Análise Exploratória e Visualização

#### Análise de Variáveis Numéricas
- Criação de histogramas com curvas de densidade para visualizar a distribuição de:
  - Tempo de Contrato
  - Custo Mensal
  - Custo Total
- Comparação visual entre clientes com e sem evasão

#### Análise de Variáveis Categóricas
- Geração de gráficos de contagem e proporção para:
  - Tipo de Contrato (Mensal, Anual, Bienal)
  - Método de Pagamento
  - Serviço de Internet (DSL, Fibra Óptica)

#### Análise de Serviços Online
- Visualização da proporção de evasão para:
  - Segurança Online
  - Backup Online
  - Proteção de Dispositivo
  - Suporte Técnico

#### Análise Específica da Fibra Óptica
- Comparação do Custo Mensal entre clientes com Fibra e DSL
- Análise da distribuição de Tipos de Contrato entre clientes com Fibra e DSL

#### Análise Demográfica
- Visualização da proporção de evasão por:
  - Gênero
  - Idoso
  - Parceiro
  - Dependentes

## Principais Descobertas

### Fatores de Alto Risco
- Contratos Mensais (taxa de evasão ~40%)
- Pagamento via Cheque Eletrônico (taxa de evasão >40%)
- Serviço de Fibra Óptica (taxa de evasão ~40%)
- Ser Idoso (taxa de evasão ~40%)
- Não ter Parceiro (taxa de evasão ~32%)
- Não ter Dependentes (taxa de evasão ~30%)
- Ausência de Segurança Online e Suporte Técnico (taxa de evasão ~30%)

### Fatores Protetores
- Contratos Anuais (~10%) e Bienais (<5%)
- Pagamentos automáticos (<15%)
- Serviço DSL (<20%)
- Ter Parceiro (taxa de evasão ~19%)
- Ter Dependentes (taxa de evasão ~15%)
- Presença de Segurança Online e Suporte Técnico (~15%)

## Recomendações Estratégicas
1. Incentivar contratos de longo prazo
2. Promover métodos de pagamento automáticos
3. Investigar e melhorar a experiência com Fibra Óptica
4. Promover serviços de valor agregado (Segurança, Suporte)
5. Desenvolver programas específicos para clientes idosos
6. Criar ofertas personalizadas para clientes sem parceiro/dependentes

## Próximos Passos
- Implementar modelos preditivos para identificar clientes com alto risco de evasão
- Realizar análise de segmentação para estratégias mais personalizadas


---

Este projeto demonstra como a análise exploratória de dados pode revelar insights valiosos para redução de churn, sem necessidade de modelos preditivos complexos.
