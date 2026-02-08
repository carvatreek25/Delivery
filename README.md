# 🛵 Delivery Analytics: Inteligência Operacional e Financeira

Este projeto apresenta uma série de análises estratégicas desenvolvidas para os times de **Marketing, Pricing e Controladoria (CFO)** de uma empresa de delivery. O foco principal é a transformação de dados brutos em indicadores de performance (KPIs) e suporte à decisão corporativa.

## 🏗️ Arquitetura de Dados e Relacionamento
<p align="center">
  <img src="imagens/relacionamento_tabelas.png" alt="Modelo de Dados e Relacionamentos" width="800">
</p>

## 🎯 Objetivos Estratégicos

O projeto foi estruturado para atender três frentes fundamentais de negócio:

### 1. Marketing & Growth
* **Top 20 Entregadores:** Identificação dos profissionais com maior distância total percorrida.
* **Mapeamento de Perfil:** Análise por tipo de profissional e modalidade de locomoção (moto, bicicleta, carro).

### 2. Estratégia de Pricing
* **Distribuição Regional:** Cálculo da distância média percorrida por motociclistas, segmentada por estado.
* **Subsídio de Taxas:** Dados estruturados para apoiar o ajuste nos valores pagos aos entregadores em cada região do país.

### 3. CFO & Diretoria Executiva
* **Análise de Receita:** Geração de indicadores de receita média e total por categoria (**Food x Goods**) e por estado.
* **Profitability & Bônus:** Cálculo do lucro líquido considerando margem de 15% e custos fixos, resultando na distribuição de bônus individual para o quadro de 2.000 funcionários.

## 📁 Estrutura do Repositório

```text
DELIVERY_PROJECT/
├── data/        # Datasets operacionais (arquivos CSV)
├── imagens/     # Diagramas de relacionamento e capturas da análise
├── notebooks/   # Desenvolvimento de EDA e modelos de cálculo
├── src/         # Scripts Python para limpeza e transformação (ETL)
├── results/     # Tabelas finais e agregações de saída
└── README.md
```