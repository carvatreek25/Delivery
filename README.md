# Delivery
Auxiliando os Times de Marketing e Pricing da Empresa de Delivery

Projeto: Análises Operacionais e Financeiras para Empresa de Delivery

📌 1. Visão Geral do ProjetoEste projeto reúne um conjunto de análises solicitadas por diferentes áreas da empresa de delivery — Marketing, Pricing e Diretoria Financeira (CFO).

O objetivo é apoiar decisões estratégicas relacionadas à performance dos entregadores, definição de preços, receita e distribuição de bônus corporativo.As análises foram conduzidas utilizando o dataset disponibilizado pela empresa, contendo informações operacionais das entregas, características dos entregadores, trajetos percorridos e valores financeiros associados às corridas.

📂 2. Estrutura do Repositório

data/ → Dataset utilizado nas análises
notebooks/ → Notebooks com etapas de exploração, modelagem e cálculos
src/ → Scripts de limpeza, transformação e cálculos
results/ → Tabelas finais e agregações solicitadas pelas áreas
README.md → Documento atual com detalhamento metodológico

🧭 3. Objetivos do ProjetoAs análises se dividem em três frentes principais:3.1 MarketingIdentificação dos 20 entregadores com maior distância total percorrida, incluindo:

Tipo de profissional
Modalidade de locomoção (ex.: moto, bicicleta, carro etc.)

3.2 Pricing

Produção da distribuição da distância média percorrida por motoqueiros, segmentada por estado, a fim de subsidiar ajustes nos valores pagos aos entregadores em cada região.3.3 CFO e Diretoria ExecutivaGeração de indicadores de receita:
Receita média e receita total por tipo de entrega (Food x Goods)
Receita média e receita total por estado

Total: 4 tabelas consolidadas.Além disso, cálculo do bônus individual a ser distribuído aos 2 mil funcionários, considerando:
Custo fixo de R$ 5,00 por entrega
Receita de 15% sobre o valor de cada entrega
Distribuição de 20% do lucro entre os funcionários

🔍 4. Metodologia
A metodologia foi estruturada em etapas sequenciais, garantindo rastreabilidade e reprodutibilidade.

4.1 Preparação dos Dados

Verificação de integridade, tipos, valores faltantes e duplicidades.
Padronização de colunas (datas, unidades de medida, estados, tipos de entrega).
Criação de variáveis auxiliares:
Distância total por entregador
Distância média por entregador
Identificação de modal de locomoção
Marcação de tipo de entrega (Food x Goods)


4.2 Análise para Marketing

Agregação por entregador:
Soma total da distância percorrida
Classificação por tipo de profissional
Modal de locomoção
Ordenação decrescente por distância total
Seleção dos 20 primeiros entregadores

4.3 Análise para Pricing

Filtragem exclusiva de entregadores com modal motocicleta
Cálculo da distância média por entrega
Agrupamento por estado

Construção da distribuição utilizando estatísticas:
Média
Mediana
Desvio padrão
Quartis


4.4 Indicadores para o CFOReceita

Para cada entrega, a receita é calculada como:receita_entrega = valor_entrega × 0.15
CustoCusto fixo por entrega:custo_entrega = 5.00
Lucro total do períodolucro = receita_total - custo_total
Montante destinado ao bônusbônus_total = lucro × 0.20
Bônus individual (2.000 funcionários)bônus_individual = bônus_total / 2000
Agregações produzidas
Receita média e total por tipo (Food x Goods)
Receita média e total por estado
As quatro tabelas geradas foram salvas na pasta results/.