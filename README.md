# Artificial-Neural-Networks
## Descrição
Essa pipeline é uma solução para análise preditiva baseada em deep learning, utilizando redes neurais artificiais (ANNs). Ele combina a validação cruzada com K-Fold e arquiteturas personalizadas de redes neurais para criar modelos robustos de regressão.

## Requisitos
- Python 3.x com bibliotecas essenciais como `numpy`, `pandas`, `scikit-learn`, `tensorflow` e `matplotlib`.
Para instalá-las, execute o seguinte comando:
```bash
pip install pandas numpy matplotlib scipy scikit-learn tensorflow
```
## Instruções de Uso
1. Certifique-se de que o arquivo de dados esteja no formato Excel `.xlsx`.
2. Substitua o caminho do arquivo na linha:
   ```python
   df = pd.read_excel("conjunto-de-dados.xlsx")
   ```
   pelo caminho do seu arquivo de dados.
3. Caso sua variável alvo já esteja presente no conjunto de dados, substitua "variavel-alvo" pela coluna correspondente.
4. Execute o script para gerar:
   - Treinamento dos dados utilizando ANNs
   - Verificação e aplicação dos melhores hiperparâmetros
   - Gráfico das métricas de treinamento
   - Gráfico de valores reais contra valores preditos
   - Métricas para avaliação de desempenho do modelo.

## Funcionalidades Principais:

Processamento de Dados:
- Importação de dados no formato Excel.
- Separação automatizada de descritores (variáveis independentes) e variável alvo (dependente).
- Validação Cruzada com K-Fold:

- Implementação de K-Fold com 5 divisões, garantindo avaliação abrangente e redução de viés nos resultados.

Normalização dos Dados:
- Uso do StandardScaler para ajustar a escala dos descritores, essencial para a convergência do modelo.

Arquitetura de Redes Neurais:
- Estrutura modular com camadas densas e Dropout para prevenir overfitting.
- Camada de saída linear para prever valores contínuos.

Treinamento Personalizado:
- Utilização do otimizador Adam para aprendizado eficiente.
- Validação durante o treinamento para monitoramento da performance.

Métricas de Avaliação:
- Geração de métricas de desempenho, como:
- Erro Quadrático Médio (MSE).
- Coeficiente de Determinação (R²).
- Erro Absoluto Médio (MAE).
- Cálculo de médias e desvios padrão para avaliar a consistência do modelo.
- Visualizações Interativas:
- Gráficos detalhados da evolução do erro ao longo das épocas de treinamento.
- Comparação entre valores previstos e reais para a última divisão do K-Fold.
