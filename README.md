# Clinical Trial Patient Matching

Este projeto faz parte da pesquisa de mestrado em Ciência da Computação, com foco em **extração de informações de protocolos clínicos** e **correspondência de pacientes elegíveis** usando **Processamento de Linguagem Natural (NLP)** e **Modelos de Linguagem de Grande Escala (LLMs)**.

## Objetivo
Desenvolver uma solução que automatize a leitura de **protocolos clínicos** (ClinicalTrials.gov) e a **extração de critérios de elegibilidade**, gerando **formulários eletrônicos** otimizados e permitindo o **ranqueamento de pacientes** a partir de bancos de dados clínicos estruturados (ex.: MIMIC-IV).

## Estrutura do Projeto
```
clinicaltrials-ia-thesis/
│
├── data/                # Dados brutos ou processados (não subir dados sensíveis)
│   ├── raw/              # Dados originais (ClinicalTrials, MIMIC, etc.)
│   └── processed/        # Dados já tratados
│
├── notebooks/           # Jupyter notebooks para experimentos
│
├── src/                 # Código fonte principal
│   ├── extraction/       # Scripts para extração de critérios do protocolo
│   ├── matching/         # Scripts para match paciente <-> protocolo
│   ├── ranking/          # Modelos de reranking e explicabilidade
│   └── utils/            # Funções auxiliares
│
├── docs/                # Documentação do projeto (metodologia, resultados)
│
├── requirements.txt     # Dependências do projeto
├── README.md            # Descrição do projeto
└── .gitignore           # Arquivos e pastas para ignorar
```

## Tecnologias e Ferramentas
- **Python 3.10+**
- **Transformers (BERT, BioBERT, PubMedBERT)**
- **Hugging Face**
- **Pandas / NumPy**
- **scikit-learn**
- **FastAPI** (para servir o modelo futuramente)
- **Streamlit** (para interface de testes)
- **MIMIC-IV** (dados clínicos)
- **ClinicalTrials.gov API** (protocolos)

## Metodologia
1. **Coleta e Pré-processamento**
   - Extração de protocolos clínicos
   - Limpeza e normalização do texto
2. **Extração de Informações**
   - Identificação de critérios de elegibilidade com **BERT/BioBERT**
3. **Geração de Formulários**
   - Uso de LLMs (ex.: GPT) para criar formulários a partir dos critérios extraídos
4. **Correspondência de Pacientes**
   - Cruzamento dos dados estruturados (MIMIC-IV) com os critérios extraídos
5. **Ranqueamento e Explicabilidade**
   - Aplicação de métricas para justificar a seleção de pacientes

## Medidas de Sucesso
- **Precisão de Extração (NER F1-score)**
- **Cobertura de Critérios**
- **Taxa de Correspondência Correta de Pacientes**
- **Avaliação por Especialistas (validação médica)**

## Contato
Para mais informações ou dúvidas, entre em contato: email: mclara.castro@hotmail.com
