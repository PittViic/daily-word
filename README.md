# Análise de Tweets do Wordle

Este projeto realiza uma análise exploratória de dados em um conjunto de tweets sobre o popular jogo de palavras Wordle. O script utiliza Python e bibliotecas de ciência de dados como `pandas`, `matplotlib` e `seaborn` para processar, analisar e visualizar padrões de jogo extraídos diretamente do texto dos tweets.

## 📊 Visão Geral

O objetivo é extrair informações valiosas sobre o comportamento dos jogadores de Wordle, como:
- O volume de tweets ao longo do tempo.
- A distribuição do número de tentativas para resolver o quebra-cabeça.
- A performance média em cada tentativa (letras corretas, no lugar errado, etc.).
- As letras mais comuns e eficazes na primeira tentativa.

---

## 🚀 Funcionalidades

O script realiza as seguintes análises e visualizações:

1.  **Processamento de Dados**:
    - Carrega o dataset de tweets.
    - Converte datas para o formato datetime.
    - Extrai o ID do Wordle e o número de tentativas diretamente do texto do tweet.

2.  **Análise Temporal**:
    - Plota um gráfico de linha mostrando o volume de tweets do Wordle por dia.

3.  **Análise de Tentativas**:
    - Cria uma tabela com gradiente de cores que mostra a distribuição do número de tentativas para cada Wordle ID.
    - Plota um gráfico de barras horizontais mostrando a contagem total de tweets para cada número de tentativas (de 1 a 6).

4.  **Análise do Conteúdo dos Tweets**:
    - Faz o parsing dos quadrados coloridos (🟩, 🟨, ⬛) para cada tentativa em cada tweet.
    - Cria novas colunas para cada uma das 6 tentativas, registrando o número de letras corretas, no lugar errado e incorretas.

5.  **Visualização de Performance por Tentativa**:
    - Gera gráficos de barras comparando a média de letras corretas, no lugar errado e incorretas para cada uma das seis tentativas.

6.  **Análise de Letras**:
    - Identifica as letras que foram adivinhadas corretamente na primeira tentativa.
    - Plota um gráfico de barras mostrando as letras mais comuns e bem-sucedidas na primeira jogada.

---

## 📋 Pré-requisitos

Para executar este script, você precisará ter o Python 3 instalado, juntamente com as seguintes bibliotecas:

-   pandas
-   numpy
-   matplotlib
-   seaborn

Você pode instalar todas as dependências necessárias com o pip:
```bash
pip install pandas numpy matplotlib seaborn
```

---

## 💾 Dataset

Este script espera um arquivo CSV chamado `tweets.csv` no mesmo diretório. O arquivo deve conter pelo menos as seguintes colunas:
-   `tweet_date`: A data e hora em que o tweet foi postado.
-   `tweet_text`: O conteúdo completo do tweet, incluindo o cabeçalho do Wordle e os quadrados coloridos.

*(Nota: O script de análise de letras requer uma coluna adicional `answer` contendo a palavra correta para cada Wordle, que não está presente no processamento inicial do script fornecido. Esta parte do código pode precisar de um dataset enriquecido para funcionar.)*

---

## ⚙️ Como Usar

1.  Clone este repositório:
    ```bash
    git clone https://github.com/PittViic/daily-word.git
    ```
2.  Navegue até o diretório do projeto:
    ```bash
    cd daily-word
    ```
3.  Coloque o seu arquivo `tweets.csv` no diretório.
4.  Execute o script Python:
    ```bash
    python seu_script.py
    ```
    Ou execute as células em um ambiente como Jupyter Notebook ou Google Colab.

---

## 📈 Exemplos de Visualizações Geradas

O script gera várias visualizações para ilustrar os padrões encontrados, incluindo:

#### Volume de Tweets por Dia
![Tweets por Dia](https://i.imgur.com/example1.png)
*Um gráfico de linha que mostra a popularidade do Wordle ao longo do tempo.*

#### Distribuição do Número de Tentativas
![Número de Tentativas](https://i.imgur.com/example2.png)
*Um gráfico de barras mostrando em quantas tentativas a maioria dos jogadores resolve o quebra-cabeça.*

#### Performance Média por Tentativa
![Performance por Tentativa](https://i.imgur.com/example3.png)
*Gráficos de barras comparando a eficácia de cada tentativa em termos de letras corretas, no lugar errado e incorretas.*

#### Letras Mais Comuns na Primeira Tentativa
![Letras da Primeira Tentativa](https://i.imgur.com/example4.png)
*Um gráfico de barras mostrando quais letras são mais frequentemente adivinhadas corretamente na primeira jogada.*

*(Nota: As imagens acima são representações ilustrativas. Substitua os links pelos gráficos reais gerados pelo seu script.)*
