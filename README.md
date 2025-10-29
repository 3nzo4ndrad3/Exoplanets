# Exoplanets — Mass–Radius Statistical Analysis

Este repositório apresenta uma análise estatística da relação entre **massa e raio de exoplanetas** utilizando modelos de **Regressão Linear** em escala logarítmica.  
O objetivo é investigar como propriedades físicas e estelares afetam o raio planetário e validar modelos preditivos para caracterização planetária.

---

## Estrutura do Projeto

| Pasta / Arquivo | Descrição |
|----------------|-----------|
| `data/exoplanets.csv` | Dataset utilizado após limpeza |
| `notebooks/EXO_RxM.ipynb` | Notebook com análise completa |
| `docs/Analise_Exoplanets.pdf` | Relatório final em PDF |
| `README.md` | Documentação do projeto |

---

## Metodologia

Foram aplicadas:

- Estatísticas descritivas e análise exploratória
- Transformações logarítmicas das variáveis físicas
- Regressão Linear Múltipla com erros robustos (HC1)
- Validação cruzada e diagnóstico dos resíduos

**Modelo final:**  
`log(R) = β₀ + β₁ · log(M) + β₂ · pl_eqt + β₃ · st_met`

---

## Principais Resultados

- Relação **sublinear** entre massa e raio (coef. ~ 0.38)
- $R^2 \approx 0.83$
- Variáveis estelares ajudam a explicar diferenças estruturais
- Modelo fisicamente consistente com a literatura atual de exoplanetologia

---

## Dataset — Licença e Citação Obrigatória

Os dados publicados aqui são derivados do:

> **NASA Exoplanet Archive**  
> https://exoplanetarchive.ipac.caltech.edu

Licença:
> Uso acadêmico e público permitido **com citação obrigatória** 

Citação recomendada:

> *This research has made use of the NASA Exoplanet Archive, which is operated by the California Institute of Technology, under contract with
> the National Aeronautics and Space Administration under the Exoplanet Exploration Program.*

---

### 🔗 Download do Dataset Original (atualizado)

Para sempre ter a última versão oficial:  
https://exoplanetarchive.ipac.caltech.edu

> A versão utilizada neste projeto corresponde aos dados disponíveis em: **Setembro/2025**

---

## Como executar

```bash
# Requisitos mínimos
Python 3.9+
pandas
numpy
matplotlib
statsmodels
scikit-learn

# Execute o notebook
jupyter notebook notebooks/EXO_RxM.ipynb
