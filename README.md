# 🏥 Sistema de Recomendação de Exames Médicos com IA Explicável

> Trabalho de Conclusão de Curso — Ciência de Dados para Negócios  
> FAE Centro Universitário — Curitiba, 2026

---

## 📋 Sobre o Projeto

Este projeto desenvolve e avalia um **sistema de recomendação de exames médicos** baseado em dados históricos de pacientes, utilizando técnicas de aprendizado de máquina e Inteligência Artificial Explicável (XAI).

A partir do perfil clínico de um paciente — diagnósticos e histórico de exames anteriores — o sistema recomenda os exames laboratoriais mais prováveis de serem solicitados, acompanhados de uma explicação gerada via **SHAP**, tornando cada recomendação transparente e auditável.

O projeto é delimitado à **validação técnica** do sistema. Não contempla implantação clínica real nem validação com pacientes em ambiente hospitalar.

---

## 👥 Equipe

| Nome | Frente |
|---|---|
| José | Dados & Código |
| Lucas | Documento (TCC) |
| Gabriel | Apresentação & Validação |

**Orientador:** a definir  
**Instituição:** FAE Centro Universitário  
**Curso:** Ciência de Dados para Negócios

---

## 🎯 Objetivo

Desenvolver e avaliar um sistema de recomendação de exames médicos baseado em dados históricos de pacientes, por meio de técnicas de aprendizado de máquina e análise de similaridade, com vistas a apoiar a tomada de decisão clínica por meio de recomendações explicáveis e mensurar seu potencial impacto na eficiência operacional e na otimização dos custos assistenciais.

---

## 🔬 Escopo Técnico (MVP)

| Item | Decisão |
|---|---|
| Base de dados | MIMIC-IV (PhysioNet — MIT) |
| Tabelas principais | `labevents`, `d_labitems`, `diagnoses_icd` |
| Abordagem | Similaridade de perfil clínico entre pacientes |
| Modelo base | Random Forest ou XGBoost |
| Explicabilidade | SHAP values |
| Métricas | Precisão@k, Recall@k |
| Linguagem | Python |
| Fora do escopo | Validação clínica real, implantação hospitalar |

---

## 🗂️ Estrutura do Repositório

```
tcc-recomendacao-exames/
├── README.md
├── notebooks/
│   ├── 01_eda.ipynb              # Análise exploratória dos dados
│   ├── 02_pipeline.ipynb         # Tratamento e feature engineering
│   └── 03_modelo_shap.ipynb      # Modelo + explicabilidade SHAP
└── docs/
    └── referencias.md            # Referências bibliográficas
```

> ⚠️ Os dados brutos do MIMIC-IV **não são versionados** neste repositório por questões de privacidade e tamanho. O acesso deve ser solicitado individualmente em [physionet.org](https://physionet.org/content/mimiciv/3.1/).

---

## 🚀 Como Executar

### Pré-requisitos
- Python 3.10+
- Jupyter Notebook ou VS Code com extensão Jupyter
- Bibliotecas: `pandas`, `scikit-learn`, `xgboost`, `shap`, `matplotlib`

### Instalação das dependências
```bash
pip install pandas scikit-learn xgboost shap matplotlib jupyter
```

### Execução
1. Baixe os dados do MIMIC-IV e coloque na pasta `dados/` (não versionada)
2. Execute os notebooks na ordem numérica: `01` → `02` → `03`

---

## 📅 Cronograma

| Sprint | Período | Foco |
|---|---|---|
| Sprint 1 | 20–26 Abr | Documento: Introdução + Fundamentação Teórica |
| Sprint 2 | 27 Abr–10 Mai | Dados MIMIC-IV + Escopo técnico fechado |
| Sprint 3 | 11–24 Mai | Construção do modelo + Metodologia |
| Sprint 4 | 25 Mai–7 Jun | MVP funcional + Documento completo |
| Sprint 5 | 8–15 Jun | Revisão, robustez e entrega final |

---

## 📚 Principais Referências

- MIMIC-IV: https://physionet.org/content/mimiciv/3.1/
- SHAP: Lundberg & Lee (2017) — *A Unified Approach to Interpreting Model Predictions*
- XAI em Saúde: George et al. (2024) — PMC11528818
- CDSS com XAI: Kim et al. (2024) — MDPI Applied Sciences

---

*FAE Centro Universitário · Curitiba · 2026*
