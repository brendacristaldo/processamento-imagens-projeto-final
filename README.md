# Classificação de Grãos de Café — Processamento de Imagens

## Equipe
-  [Ana Beatriz Maciel Ferraz](https://github.com/anabmferraz)
- [Brenda Cristaldo](https://github.com/brendacristaldo)
- [Werickson Dauta](https://github.com/Wericksonsd)

## Descrição da Abordagem

O projeto aplica a abordagem clássica de classificação de imagens, composta por duas etapas principais: extração de características e classificação.

**Extração de características:** foram utilizados Filtros de Gabor, que capturam informações de textura e frequência espacial das imagens em diferentes orientações (0°, 45°, 90°) e frequências (0.1, 0.3, 0.5). Para cada combinação de orientação e frequência, foram extraídas a média e a variância da resposta do filtro, resultando em um vetor de 18 características por imagem.

**Classificador:** Support Vector Machine (SVM) com kernel RBF (Radial Basis Function), com parâmetros C=10 e gamma='scale'. Os dados foram normalizados com StandardScaler antes da classificação.

## Dataset

- **Nome:** Coffee Bean Dataset Resized (224 x 224)
- **Classes:** Dark, Green, Light, Medium
- **Total de imagens:** 1600 (1200 treino, 400 teste)
- **Formato:** imagens coloridas RGB 224×224 pixels
- **Link:** https://www.kaggle.com/datasets/gpiosenka/coffee-bean-dataset-resized-224-x-224

## Resultados

| Métrica | Valor |
|---|---|
| Acurácia | 86,75% |
| Precisão (macro avg) | 87% |
| Recall (macro avg) | 87% |
| F1-score (macro avg) | 87% |

### Resultados por classe

| Classe | Precisão | Recall | F1-score |
|---|---|---|---|
| Dark | 0.86 | 0.87 | 0.87 |
| Green | 0.91 | 0.90 | 0.90 |
| Light | 0.84 | 0.87 | 0.85 |
| Medium | 0.86 | 0.83 | 0.85 |

## Bibliotecas Utilizadas
- Python 3
- OpenCV
- scikit-image (Filtros de Gabor)
- scikit-learn (SVM, StandardScaler, métricas)
- NumPy
- Matplotlib

## Links
- Vídeo de apresentação: 

## Instruções de Uso
1. Abrir o notebook no Google Colab
2. Fazer download do dataset pelo Kaggle API ou manualmente
3. Extrair o dataset na pasta `/content/dataset`
4. Executar as células em ordem
