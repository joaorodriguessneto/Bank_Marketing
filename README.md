![Imagem inicial](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/img_readme_inicial.png)
# 📊 Análise de campanhas bancárias e previsão de adesão de clientes

## 🔍 Observações Relevantes sobre o Projeto:

#### Neste projeto, será realizada uma análise das campanhas de marketing do Banco Aurora, explorando variáveis demográficas, financeiras e comportamentais dos clientes. O estudo busca compreender os fatores que influenciam a adesão, identificar perfis com maior propensão à conversão e desenvolver um modelo preditivo de classificação com algoritmos de boosting. O produto analisado é o depósito a prazo, um investimento seguro em que o cliente aplica seu próprio dinheiro no banco por um período determinado, recebendo juros ao final do prazo. A partir disso, serão gerados insights estratégicos para otimizar campanhas, reduzir custos e direcionar recursos de forma mais eficiente.



## 🎯 Desafio: Predição de Adesão de Clientes a Empréstimos do Banco Aurora



#### Neste projeto, vamos utilizar modelos de boosting, como o Gradient Boosting, para analisar o comportamento dos clientes do Banco Aurora. Nosso objetivo será retirar insights dos dados, identificando padrões que nos ajudem a entender quem terá maior propensão a aderir aos produtos financeiros.
#### Vamos realizar encoding de variáveis categóricas para que os modelos interpretem corretamente as informações e, em seguida, plotar gráficos para facilitar a visualização das variáveis mais relevantes.
#### Com o modelo de classificação do Gradient Boosting, pretendemos definir o melhor modelo para o projeto e identificar o perfil de cliente mais propenso a contratar o empréstimo, apoiando decisões estratégicas de marketing.


## ❓ Questionamentos do CEO:

* Identificar padrões e perfis de clientes que mais aderem às ofertas.

* Otimizar as estratégias de marketing, reduzindo o custo por aquisição.

* Construir um modelo preditivo de classificação, capaz de indicar a probabilidade de um cliente aderir à campanha.


## 🗂️Dicionário dos dados fornecidos pelo banco:

  * age – Idade do cliente em anos;
    * job – Ocupação ou profissão do cliente,;
    * marital – Estado civil do cliente;
        * married → casado(a)
        * single → solteiro(a)
        * divorced → divorciado(a)
    * education – Nível de escolaridade do cliente;
        * secondary → ensino médio
        * tertiary → ensino superior
        * primary → ensino fundamental
        * unknown → desconhecido
    * default – Indica se o cliente possui histórico de inadimplência em crédito (sim ou não);
    * balance – Saldo médio anual da conta do cliente em euros;
    * housing – Indica se o cliente possui empréstimo habitacional (sim ou não);
    * loan – Indica se o cliente possui empréstimo pessoal (sim ou não);
    * contact – Meio de contato utilizado na última campanha, como telefone ou e-mail;
    * day – Dia do mês em que o cliente foi contatado na campanha;
    * month – Mês em que o cliente foi contatado na campanha;
    * duration – Duração do último contato com o cliente em segundos;
    * campaign – Número de contatos realizados durante a campanha atual para este cliente;
    * pdays – Número de dias desde o último contato em campanhas anteriores (-1 se não houver);
    * previous – Número de contatos realizados em campanhas anteriores;
    * poutcome – Resultado da campanha anterior, como sucesso, fracasso ou inexistente;
    * deposit – Variável alvo que indica se o cliente aderiu à oferta de depósito a prazo
        * Sim - cliente aderiu
        * Não - cliente não aderiu

    

## 🛠️ Abordagem Atual da Empresa (Método utilizado atualmente) 


* #### Atualmente, o Banco Aurora realiza suas campanhas de marketing com base em análises históricas simples e critérios gerais de segmentação, contando em grande parte com a experiência da equipe de marketing para definir quais clientes serão contatados.
* #### Como cientista de dados do banco, nosso objetivo será aprimorar esse processo, tornando-o mais preciso e baseado em evidências. Para isso, será desenvolvido um modelo de machine learning de classificação, utilizando algoritmos como Gradient Boosting, CatBoost e redes neurais, capaz de prever a probabilidade de um cliente aderir a produtos financeiros, identificando os perfis de maior propensão e auxiliando na definição de estratégias mais eficazes de marketing.


 # 🧠 Principais insights da análise exploratória 

 #### Após a análise realizada, será possível identificar que as características que mais influenciam a adesão dos clientes aos produtos financeiros, dentro do conjunto de dados analisado, serão: o perfil do cliente, tipo de contato, mês em que o cliente foi contatado, a renda mensal, a idade e outros fatores comportamentais relevantes.

 * ##  Saldo Médio Anual

![gráfico de barras](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/distribuicao_balance.png)

#### O gráfico apresenta a distribuição do saldo médio anual do cliente, em que ns mostra que mais de 5000 clientes mantém uma média de até 1000 Euros na sua conta por ano.

* ##  Adesão ao Empréstimo pelo Saldo Médio Anual

![gráfico de barras](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/adesao_balance.png)

#### O gráfico revela que a maior adesão vem dos clientes com saldo médio anual de até 1.000 euros, representando cerca de 3.000 pessoas, ou aproximadamente 55% do total de 5.500 clientes. Logo em seguida, vemos uma boa adesão também entre aqueles com saldo entre 1.000 e 5.000 euros, mostrando que tanto clientes com menor quanto com médio saldo têm interesse nos produtos do banco.

* ##  Mês do Contato

![gráfico de barras](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/distribuicao_month.png)

#### O gráfico mostra a distribuição dos meses em que os clientes foram contatados pelo banco. Percebemos que maio é o mês com maior número de contatos, atingindo aproximadamente 3.000 clientes, seguido pelos meses de agosto e julho, indicando períodos em que a comunicação com os clientes é mais intensa.

* ##  Adesão Mês do Contato

![gráfico de barras](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/adesao_month.png)

#### O gráfico mostra que, embora o depósito a prazo tenha sido oferecido a um grande número de clientes, cerca de 3.000 pessoas, apenas aproximadamente 900 clientes efetivamente aderiram ao produto. Essa diferença evidencia que a adesão nem sempre acompanha o volume de ofertas, destacando a importância de entender melhor o perfil dos clientes e o momento do contato.

* ##  Tipo do Contato

![gráfico de pizza](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/distribuicao_contact.png)

#### O gráfico apresenta a distribuição dos tipos de contato realizados pelo banco. Observa-se que a maior parte, cerca de 72%, é feita por celular, atualmente o meio de comunicação mais utilizado e confiável. Em seguida, 21% dos contatos não tiveram o meio informado, enquanto apenas 6,9% foram realizados por telefone. Esses dados mostram a predominância dos celulares como canal principal de comunicação com os clientes.

* ##  Adesão ao Depósito a Prazo pelo Tipo do Contato

![gráfico de pizza](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/adesao_contact.png)

#### O gráfico mostra a adesão dos clientes ao depósito a prazo de acordo com o tipo de contato realizado pelo banco. Observa-se que, de aproximadamente 8.000 clientes contatados, cerca de 4.500 clientes que receberam contato via celular aderiram ao produto financeiro, evidenciando a eficácia desse canal como principal meio de comunicação e conversão.

# 📈Avaliação do Gradient Boosting: Performance e Melhor Estimador

#### Foram realizados experimentos utilizando Grid Search, Randomized Search e Bayesian Search para os modelos XGBoost, LightGBM e CatBoost, com o objetivo de aprofundar os conhecimentos em otimização de hiperparâmetros. Para o desenvolvimento final do projeto, o modelo escolhido será o Bayesian Search, por apresentar melhor desempenho e eficiência na busca dos parâmetros ideais.

* ##  XGBoost

* ### XGBoost Default

![Melhores metricas do XGBoost Default](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/metricas_xgboost_default.png)

#### Os valores acima apresentam as métricas do XGBoost Default, ou seja, o modelo sem qualquer otimização de hiperparâmetros.

* ### Grid Search

![Melhores parâmetros do Grid Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/grid_search_xgboost_best_params.png)

#### Os valores acima apresentam os melhores parâmetros obtidos pelo Grid Search, servindo como referência para comparação posterior com os resultados do Bayesian Search e do Randomized Search.

![Melhores estimadores do Grid Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/grid_search_xgboost_best_estimator.png)

#### Os valores acima apresentam os melhores estimadores obtidos pelo Grid Search, o que servirá como referência para comparação posterior com os resultados do Bayesian Search e do Randomized Search.

![Melhores metricas do Grid Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/Metricas_Hiperparametros_XGBoost_GridSearch.png)

#### Os valores acima apresentam as métricas obtidas pelo Grid Search para o XGBoost.

* ### Randomized Search

![Melhores parâmetros do Randomized Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/randomized_search_xgboost_best_params.png)

#### Os valores acima apresentam os melhores parâmetros obtidos pelo Randomized Search, servindo como referência para comparação com os resultados do Bayesian Search e do Grid Search.

![Melhores estimadores do Randomized Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/randomized_search_xgboost_best_estimator.png)

#### Os valores acima apresentam os melhores estimadores obtidos pelo Randomized Search, servindo como referência para a comparação com os resultados do Bayesian Search e do Grid Search.

![Melhores metricas do Randomized Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/Metricas_Hiperparametros_XGBoost_RandomizedSearch.png)

#### Os valores acima apresentam as métricas obtidas pelo Randomized Search para o XGBoost.

* ### Bayesian Search

![Melhores parâmetros do Bayesian Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/bayes_search_xgboost_best_params.png)

#### Os valores acima apresentam os melhores parâmetros obtidos pelo Bayesian Search, servindo como referência para comparação com os resultados do Randomized Search e do Grid Search.

![Melhores metricas do Bayesian Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/Metricas_Hiperparametros_XGBoost_BayesSearch.png)

#### Os valores acima apresentam as métricas obtidas pelo Bayesian Search para o XGBoost.

* ##  LightGBM

![Melhores metricas do LightGBM](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/Metricas_Hiperparametros_LGBM_BayesSearch.png)

#### Os valores acima apresentam as métricas obtidas pelo Bayesian Search para o LightGBM.

* ##  CatBoost

![Melhores metricas do CatBoost](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/Metricas_Hiperparametros_LGBM_BayesSearch.png)

#### Os valores acima apresentam as métricas obtidas pelo Bayesian Search para o CatBoost.


* ##  Tabela Comparativa

![Melhores metricas do Bayesian Search](https://github.com/joaorodriguessneto/Bank_Marketing/blob/main/img/TABELA_METRICAS_COMPARATIVA.png)

#### Tendo em vista a tabela acima, o XGBoost será nosso modelo principal neste projeto por apresentar excelente desempenho em precisão e acurácia, métricas fundamentais para direcionar campanhas de marketing de forma eficiente. Com uma precisão de 84,6% e acurácia de 81,21%, ele consegue identificar de maneira confiável os clientes com maior probabilidade de aderir ao depósito a prazo, evitando esforços desnecessários com contatos que provavelmente não resultarão em adesão.
#### Embora o LightGBM e o CatBoost capturem uma quantidade maior de clientes que realmente aderem (recall mais alto), eles também apresentam muitos falsos positivos, o que poderia gerar desperdício de recursos. Por isso, o XGBoost se destaca, garantindo que as predições positivas sejam mais confiáveis e que as campanhas sejam mais estratégicas e assertivas.