# Projeto: Projeto Final - Identifique perfis de consumidores de e-commerce

**Objetivos de pesquisa:**
Bem-vindo ao nosso projeto de ofertas personalizadas para usuários da Everything Plus, loja online de venda de utensílios domésticos. Nosso cliente é o gerente de produto responsável pela experiência do usuário, que solicitou nossa análise para ajudar a fazer ofertas personalizadas para os usuários. Os usuários pretendidos do nosso resultado final são os clientes que solicitaram a análise.

Nosso objetivo é analisar todo o período coberto pelos dados de origem, que contém o histórico de transações do Everything Plus. O conjunto de dados, denominado ecommerce_dataset_us.csv, contém várias colunas, incluindo identificadores de pedidos e itens, nomes de itens, data do pedido, preço por item e ID do cliente.

A necessidade desta pesquisa surgiu porque a pesquisa qualitativa por si só não é suficiente para tomar decisões informadas. Portanto, analisaremos os dados para fornecer argumentos baseados em fatos e números. Este tipo de pesquisa nunca foi realizada pela Everything Plus antes, tornando o nosso projeto uma oportunidade única e emocionante.

Nossa solução envolverá a análise dos dados para identificar padrões e tendências que podem ajudar a personalizar as ofertas para os usuários. Forneceremos insights e recomendações detalhadas com base nos dados para ajudar o gerente de produto e os clientes a tomar decisões informadas.

**Objetivos:**
- Limpe e prepare dados
- Realizar análise exploratória de dados e visualizar métricas
- Segmentar usuários com base em seus perfis de consumo.
- Avaliar a segmentação de usuários e responder perguntas
- Formular e testar hipóteses estatísticas
- Apresentar conclusões e recomendações básicas

**Questões:**
1. Existem segmentos de clientes que só fazem compras em determinadas estações ou épocas do ano?
2. Existem segmentos de clientes que são compradores recorrentes há muito tempo?
3. Existem segmentos de clientes que repetiram compras em um curto espaço de tempo?
4. Existem segmentos de clientes que fazem grandes encomendas e que padrões podem ser observados no seu comportamento de compra?
5. Existem segmentos de clientes que fazem principalmente pedidos no atacado?
6. Existem segmentos de clientes que anteriormente gastavam muito ou eram compradores frequentes, mas que desde então pararam de fazer compras e permaneceram inativos por um longo período de tempo?

| Column names | Description |
|-|-------------|
| InvoiceNo | order identifier |
| StockCode | item identifier |
| Description | item name |
| Quantity |  |
| InvoiceDate | order date |
| UnitPrice | price per item |
| CustomerID |  |

**Apresentação / Dashboard:**

[PDF de apresentação](https://drive.google.com/drive/folders/1gslZ4Osf7-vBGqRZu8KzUt81o1CX0N_z?usp=sharing)

[Dashboard](https://public.tableau.com/app/profile/katia.goldchleger/viz/Dashboard_Final_Project_17100040077720/Storytelling?publish=yes)

-----

**Conclusões Finais**

Neste projeto, o objetivo principal foi analisar o histórico de transações do Everything Plus. O projeto envolveu diversas etapas e técnicas, que são resumidas a seguir:
1. **Preparação de dados:**
    - Começamos limpando e preparando os dados. Isso incluiu várias tarefas, como renomear colunas, converter tipos de dados, remover entradas duplicadas, tratar valores ausentes, eliminar valores discrepantes e descartar dados irrelevantes.
    - Como resultado, cerca de 8.174 linhas, que representavam 0,985% das 541.909 linhas originais, foram eliminadas dos conjuntos de dados.
-----
2. **Análise Exploratória de Dados:**
    - Realizamos análise exploratória de dados e visualizamos diversas métricas. Nossa análise mostrou que a Everything Plus gera uma receita média de US$ 33.571 diariamente com a venda de 18.102 unidades de 1.742 produtos, que são adquiridos por 67 clientes.
    - Também notamos um aumento nas tendências de receita durante a temporada de férias. Testaremos essa hipótese em uma seção posterior por meio de testes estatísticos.
-----
3. **Segmentação de usuários:**
    - Realizamos segmentação de usuários usando análise RFM e agrupamento K-Means.
    - Para avaliar os resultados do agrupamento, comparamos diversas métricas como Silhouette Score, Calinski Harabaz Index e Davies Bouldin Index
    - A análise de clustering de usuários revelou cinco clusters de clientes.
        - O cluster 0 representa clientes de baixo valor que não contribuem muito para a receita e que não valem a pena perseguir.
        - O Cluster 1 consiste em clientes fiéis que fazem compras frequentes e geram receitas moderadas.
        - O Cluster 2 é composto por novos clientes que fizeram compras recentes, mas ainda não contribuíram significativamente para a receita, e devem ser alvo de promoções para convertê-los em potenciais fidelizados.
        - O Cluster 3 é o cluster dos grandes gastadores e é essencial proporcionar-lhes ofertas e promoções especiais para incentivar a repetição de compras.
        - O Cluster 4 é um potencial cluster leal que poderia levar a um aumento significativo nas receitas se convertido em clientes fiéis.
    - Realizaremos testes estatísticos para determinar se há uma diferença significativa entre os clusters.
4. **Respondendo às perguntas:**
    - Q1: Existem segmentos de clientes que só fazem compras durante determinadas estações ou épocas do ano?
        - A1: Nenhum segmento apresenta comportamento sazonal distinto, mas maiores tamanhos de compras em novembro e dezembro podem ser devido à temporada de férias.
    - Q2: Existem segmentos de clientes que são compradores recorrentes há um longo período de tempo?
        - A2: Cluster 2 (clientes fiéis) apresenta alta frequência de compra e alta contagem de meses com transações.
    - Q3: Existem segmentos de clientes que repetiram compras em um curto espaço de tempo?
        - A3: Não foi identificado nenhum segmento que faça compras repetidas em um curto espaço de tempo.
    - Q4: Existem segmentos de clientes que fazem grandes encomendas e que padrões podem ser observados no seu comportamento de compra?
        - A4: Clientes que fazem grandes pedidos tendem a ter baixa frequência, mas alguns no Cluster 4 apresentam comportamento de compra de alto tamanho. A equipe de marketing deve se concentrar em aumentar a frequência de compra.
    - Q5: Existem segmentos de clientes que fazem principalmente pedidos no atacado?
        - A5: O cluster 0 (cliente de baixo valor) e o cluster 2 (novo cliente) apresentam comportamento de compra no atacado.
    - P6: Existem segmentos de clientes que anteriormente gastavam muito ou eram compradores frequentes, mas que desde então pararam de fazer compras e ficaram inativos por um longo período de tempo?
        - A6: Nenhum cliente possui valores altos tanto monetários quanto recentes. Os clientes que não fizeram compras recentemente (cluster 0) nunca fizeram contribuições significativas para a receita, enquanto aqueles que gastaram muito dinheiro (clusters 1 e 3) fizeram compras recentes e frequentes.
-----
5. **Resultados do teste de hipóteses:**
    - O teste de hipótese refuta a sobreposição entre a atualidade de novos clientes e potenciais fiéis na visualização de agrupamento 2D, indicando uma diferença significativa entre seus valores médios de atualidade.
    - O teste de hipótese apoia o argumento da visualização de agrupamento de que clientes fiéis e potenciais fidelizados podem ser diferenciados pela frequência de compra, com uma diferença significativa entre os seus valores médios de frequência.
    - O teste de hipóteses apoia o argumento da visualização de agrupamento de que os clientes fiéis e os grandes gastadores podem ser diferenciados pela contribuição monetária, com uma diferença significativa entre os seus valores monetários médios.
    - O teste de hipótese comprovou que não há diferença significativa nas receitas geradas pelas compras realizadas no período de festas de fim de ano em relação aos demais meses.
    - O teste de hipóteses comprovou que não há diferença significativa na quantidade média de compras realizadas no período de festas de fim de ano em relação aos demais meses.
