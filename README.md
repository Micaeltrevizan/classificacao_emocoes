# Análise de Texto com Random Forest

Este projeto consiste em dois scripts Python que realizam a preparação de dados e a aplicação de um modelo Random Forest para análise de texto.

## Descrição Geral

O primeiro script, `Preparação_Dados_Treinamento.py`, carrega um conjunto de dados de texto, realiza o pré-processamento necessário (codificação de variáveis categóricas, escalonamento) e divide os dados em conjuntos de treinamento e teste. O segundo script carrega os dados pré-processados, treina um modelo Random Forest e avalia seu desempenho.

## Arquivos

* **`Preparação_Dados_Treinamento.py`**: Script para carregar, pré-processar e dividir os dados.
* **`base.pkl`**: Arquivo pickle contendo os dados pré-processados e divididos.
* **`text.csv`**: Arquivo CSV contendo os dados de texto originais.

## Dependências

* `pandas`
* `numpy`
* `seaborn`
* `plotly`
* `matplotlib`
* `scikit-learn`
* `pickle`

## Preparação_Dados_Treinamento.py

### Funcionalidades

1.  **Carregamento de Dados**: Carrega os dados de um arquivo CSV (`text.csv`).
2.  **Visualização de Dados**: Exibe as primeiras e últimas linhas dos dados, estatísticas descritivas e a distribuição da variável alvo (`label`).
3.  **Pré-processamento de Dados**:
    * Separa os dados em previsores (`x_base`) e variável alvo (`y_base`).
    * Codifica variáveis categóricas usando `LabelEncoder` e `OneHotEncoder`.
    * Escala os dados usando `StandardScaler`.
4.  **Divisão de Dados**: Divide os dados em conjuntos de treinamento e teste usando `train_test_split`.
5.  **Salvamento de Dados**: Salva os conjuntos de treinamento e teste em um arquivo pickle (`base.pkl`).

### Uso

1.  Certifique-se de que o arquivo `text.csv` esteja no mesmo diretório ou forneça o caminho correto.
2.  Execute o script `Preparação_Dados_Treinamento.py`.
3.  O arquivo `base.pkl` será criado com os dados pré-processados.

## Random Forest (Text)

### Funcionalidades

1.  **Carregamento de Dados**: Carrega os dados pré-processados do arquivo pickle (`base.pkl`).
2.  **Imputação de Dados**: Imputa valores ausentes nos dados de treinamento usando `SimpleImputer`.
3.  **Treinamento do Modelo**: Treina um modelo Random Forest usando os dados de treinamento.
4.  **Previsões**: Realiza previsões nos dados de teste.
5.  **Avaliação do Modelo**: Calcula a acurácia e exibe o relatório de classificação do modelo.

### Uso

1.  Certifique-se de que o arquivo `base.pkl` esteja no mesmo diretório.
2.  Execute o script.
3.  A acurácia e o relatório de classificação do modelo serão exibidos.

## Como Executar

1.  Instale as dependências usando pip:

    ```bash
    pip install pandas numpy seaborn plotly matplotlib scikit-learn
    ```

2.  Execute o script `Preparação_Dados_Treinamento.py` para gerar o arquivo `base.pkl`.

    ```bash
    python Preparação_Dados_Treinamento.py
    ```

3.  Execute o script de Random Forest para treinar e avaliar o modelo.

    ```bash
    python seu_script_random_forest.py
    ```

## Observações

* O arquivo `text.csv` deve estar no formato correto para que o script funcione.
* Os parâmetros do modelo Random Forest podem ser ajustados para melhorar o desempenho.
* A imputação de dados é realizada apenas nos dados de treinamento.
* O arquivo pickle (`base.pkl`) é usado para transferir os dados entre os scripts.
