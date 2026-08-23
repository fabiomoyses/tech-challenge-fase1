# Tech Challenge: Previsão de NPS no E-commerce

## Objetivo do Projeto
O objetivo deste projeto é investigar a variabilidade no Net Promoter Score (NPS) de um e-commerce em crescimento. Através da análise de dados operacionais (logística e atendimento), o projeto visa identificar os principais atritos na experiência do cliente e construir um modelo preditivo capaz de estimar a nota de NPS antes da aplicação da pesquisa. Isso permite à empresa atuar de forma proativa na retenção e recuperação de detratores.

## Descrição da Base de Dados
A base de dados (`desafio_nps_fase_1.csv`) contém 2.500 registros históricos de compras. Ela engloba:
* **Dados do pedido:** valor, quantidade de itens, parcelas e descontos.
* **Dados logísticos:** tempo de entrega, dias de atraso e tentativas de entrega.
* **Dados de atendimento:** número de contatos no SAC, contagem de reclamações e tempo de resolução.
* **Variável Alvo:** `nps_score` (escala contínua de 0 a 10).

## Metodologia Utilizada
O projeto foi desenvolvido seguindo os preceitos de Ciência de Dados orientada a negócios:
1. **Análise Exploratória de Dados (EDA):** Identificação de gargalos operacionais e perfil de detratores/promotores.
2. **Análise Estatística:** Validação de variáveis utilizando testes de Correlação Paramétricos (Pearson) e Não-Paramétricos (Spearman e Kendall).
3. **Modelagem Preditiva:** Separação dos dados (80% treino / 20% teste) utilizando padrão hold-out (`train_test_split`). Treinamento de algoritmos utilizando Regressão Linear (OLS) via `statsmodels`. Foram comparados cenários de modelo simples (focado em atraso) vs. múltiplo (jornada completa).
4. **Avaliação de Performance:** Utilização das métricas MAE, MSE e RMSE via `scikit-learn` para atestar a capacidade preditiva do modelo nos dados inéditos de teste.

## Como Reproduzir os Resultados
Para reproduzir este projeto em sua máquina local, siga os passos abaixo:

1. Faça o clone deste repositório:
   ```bash
   git clone [https://github.com/fabiomoyses/tech-challenge-fase1.git](https://github.com/fabiomoyses/tech-challenge-fase1.git)