# German Credit Risk Prediction – Modelagem e Otimização de Custo (End-to-End)

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3%2B-orange)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-2.0%2B-green)](https://xgboost.readthedocs.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Estudo de caso completo em ML: prever risco de crédito minimizando o custo financeiro do banco.**

---

## Objetivo de Negócio: Minimização do Prejuízo

| Erro | Significado | Custo |
|------|-------------|-------|
| **FN** | Aprovar mau pagador | **5x** |
| **FP** | Negar bom pagador | **1x** |

**Fórmula:** $Custo = 5 \times FN + 1 \times FP$

---

## Habilidades Demonstradas

| Categoria | Técnicas |
|---------|----------|
| **Pipeline** | `ColumnTransformer`, `OneHotEncoder`, `StandardScaler` |
| **Modelos** | `RandomForest`, `XGBoost`, `LogisticRegression` |
| **Desbalanceamento** | `SMOTE`, `class_weight`, `scale_pos_weight` |
| **Otimização** | **Threshold Tuning** para custo mínimo |
| **Avaliação** | `ROC-AUC`, `classification_report`, custo customizado |

---

## Resultados: Menor Custo ≠ Maior Acurácia

| Modelo | Acurácia | **Custo Mínimo** | AUC |
|--------|----------|------------------|-----|
| **RF Ponderado + Limiar Otimizado** | 0.740 | **170** | 0.794 |
| Logistic Regression | **0.783** | 233 | 0.803 |
| XGBoost | 0.727 | 262 | 0.778 |

> **Economia de 27% no prejuízo** com modelo de menor acurácia, mas **melhor alinhado ao negócio**.

---

## Como Executar (Passo a Passo)

1. **Clone o repositório**
   ```bash
   git clone https://github.com/jean-c-silva/german-credit-risk.git
   cd german-credit-risk