# Trabalho de Inteligência Artificial — SmartMaintenance ⚙️

## Sistema Especialista para Diagnóstico e Prevenção de Falhas Industriais

Este repositório contém o projeto acadêmico **SmartMaintenance**, desenvolvido para a disciplina de Inteligência Artificial.

O projeto demonstra a aplicação prática de duas abordagens complementares de Inteligência Artificial: sistemas especialistas baseados em regras e aprendizado de máquina (*Machine Learning*).

## 📌 Sobre o projeto

O **SmartMaintenance** é uma aplicação desenvolvida em Python para diagnóstico e prevenção de riscos de falhas em máquinas industriais.

O sistema combina:

- **Sistema Especialista:** utiliza regras SE–ENTÃO e mecanismos de inferência progressiva (*Forward Chaining*) e retrogressiva (*Backward Chaining*).
- **Machine Learning:** utiliza um modelo Random Forest para estimar a ocorrência de falhas a partir de parâmetros operacionais.
- **Interface interativa:** permite inserir dados, investigar hipóteses, visualizar resultados e comparar as conclusões dos dois mecanismos.

## 🛠️ Tecnologias principais

- Python 3.11+
- Streamlit
- Pandas e NumPy
- Scikit-learn
- Plotly
- Pytest

## 📂 Organização do repositório

```text
Trabalho_Bia/
│
├── README.md
├── Makefile
├── .vscode/
│   └── settings.json
│
└── SmartMaintenance/
    ├── app.py
    ├── knowledge/
    ├── engine/
    ├── machine_learning/
    ├── interface/
    ├── data/
    ├── models/
    ├── tests/
    ├── docs/
    ├── requirements.txt
    └── README.md
```

## 🚀 Como acessar e executar

Acesse a pasta [`SmartMaintenance/`](SmartMaintenance/) para encontrar o código-fonte e a documentação completa do projeto.

O manual interno apresenta:

- Instruções de instalação e configuração do ambiente Python.
- Comandos para executar a aplicação Streamlit.
- Procedimentos para treinar o modelo de Machine Learning.
- Execução dos testes automatizados.
- Descrição da arquitetura e dos algoritmos utilizados.

**Documentação completa:** [SmartMaintenance/README.md](SmartMaintenance/README.md)

## ⚠️ Aviso acadêmico

Este projeto possui finalidade exclusivamente educacional e demonstrativa. Os resultados e recomendações não devem ser utilizados como substitutos de sistemas certificados de monitoramento, manutenção ou segurança industrial.

---

Desenvolvido como projeto acadêmico para a disciplina de Inteligência Artificial.
