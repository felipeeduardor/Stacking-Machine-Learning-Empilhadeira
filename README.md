# Stacking - Empilhamento de Algoritmos de Machine Learning

Implementação da técnica de **Stacking (Ensemble Learning)** utilizando o scikit-learn, comparando modelos base individualmente com o modelo empilhado final.

---

## O que é Stacking?

Stacking é uma técnica de aprendizado de máquina conjunto que combina as previsões de **dois ou mais modelos base** usando um **meta-learner**, que aprende a melhor forma de combiná-los.

O benefício do empilhamento é que ele pode aproveitar os recursos de uma variedade de modelos de bom desempenho e fazer previsões que têm **melhor desempenho do que qualquer modelo individual**.

```
Dados de entrada
      │
      ├──► Logistic Regression ──┐
      ├──► KNN                   │
      ├──► Decision Tree    ──►  Meta-Learner (LR)  ──► Predição Final
      ├──► SVM                   │
      └──► Naive Bayes      ──┘
```

---

## Resultados

### Modelos Base (Level 0)

| Modelo               | Acurácia Média | Desvio Padrão |
|----------------------|---------------|---------------|
| Logistic Regression  | 86.6%         | ±2.9%         |
| KNN                  | 93.1%         | ±2.5%         |
| Decision Tree (CART) | 82.8%         | ±4.3%         |
| SVM                  | 95.7%         | ±2.0%         |
| Naive Bayes          | 83.3%         | ±3.1%         |

### Stacking vs Melhor Modelo Individual

| Modelo        | Acurácia Média |
|---------------|---------------|
| SVM (melhor)  | 95.7%         |
| **Stacking**  | **96.5%**     |

> O Stacking superou todos os modelos individuais.

---

## Tecnologias

- Python 3
- scikit-learn
- NumPy
- Matplotlib

---

## Como executar

```bash
# Clone o repositório
git clone https://github.com/felipeeduardor/Stacking-Machine-Learning-Empilhadeira.git

# Instale as dependências
pip install scikit-learn numpy matplotlib

# Abra o notebook
jupyter notebook
```

---

## Estrutura do Projeto

```
├── Telegram Desktop/
│   └── 16_21_Stacking_Machine_Learning_Empilhamento_de_Algoritmos.ipynb
└── README.md
```

---

## Aplicações no Mundo Real

Esta técnica pode ser aplicada em problemas como:

- **Financeiro** — Previsão de inadimplência de crédito
- **Saúde** — Diagnóstico de doenças
- **E-commerce** — Previsão de churn de clientes
- **Marketing** — Classificação de leads
- **RH** — Previsão de turnover de funcionários

---

## Créditos

Conteúdo baseado nas aulas do **Bootcamp CDP** — [Ciência dos Dados](https://cienciadosdados.com)
