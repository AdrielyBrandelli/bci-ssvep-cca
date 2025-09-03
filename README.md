# bci-ssvep-cca
# Atividade Prática – BCI com CCA e SSVEP

Este repositório contém minha atividade prática da disciplina *IA006 – Introdução a Interfaces Cérebro-Computador*, cursada como aluna especial na Unicamp (1º semestre de 2025). A atividade foi desenvolvida com apoio de ferramentas de IA e bibliotecas científicas em Python.

---

## Objetivos

- Construir uma BCI baseada em potenciais visualmente evocados em regime estacionário (SSVEP)  
- Implementar o algoritmo de Análise de Correlação Canônica (CCA)  
- Avaliar o impacto da duração da janela de EEG e do número de harmônicas no desempenho do sistema  

## Conteúdo

- `relatorio.pdf`: relatório técnico com análise dos resultados
- `questoes.md`: questões teóricas da atividade
- `notebook.ipynb`: notebook original com código base em Python


## Base de dados

Utiliza o [Benchmark Dataset da Universidade de Tsinghua](https://bci.med.tsinghua.edu.cn/download.html), com sinais de EEG de 64 eletrodos. Para esta atividade, foram considerados apenas os eletrodos da região occipital e proximidades: Pz, PO5, PO3, POz, PO4, PO6, O1, Oz, O2.

## Metodologia

- Extração de janelas de EEG com início fixo em 0,64 s após o início da estimulação  
- Implementação do CCA para correlação entre sinais de EEG e sinais de referência (frequência fundamental + harmônicas)  
- Cálculo de acurácia e taxa de transferência de informação (ITR) para diferentes durações de janela (0,5 s a 5 s) e número de harmônicas (0 a 5)  
- Comparação entre voluntários 3 e 21

## Resultados

- Gráficos de correlação (ρm) vs frequência de estímulo  
- Curvas de acurácia e ITR em função da duração da janela e número de harmônicas  
- Discussão sobre latência de evocação, desempenho por voluntário e impacto das configurações

## Tecnologias utilizadas

- Python  
- Bibliotecas: `numpy`, `scipy`, `matplotlib`, `sklearn`  
- Algoritmo CCA implementado em modo não-supervisionado  
- Cálculo de ITR conforme fórmula padrão com gaze shifting time de 0,55 s

## Referências

- Lin et al., 2006 – *Frequency recognition based on canonical correlation analysis for SSVEP-based BCIs*, IEEE T-BME  
- Wang et al., 2017 – *A Benchmark Dataset for SSVEP-Based Brain–Computer Interfaces*, IEEE TNSRE
