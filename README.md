# Previsão de Estados Emocionais com NeuroBERT-Tiny e Fine-Tuning

## Visão Geral do Projeto

Este repositório contém o protótipo de um modelo de Inteligência Artificial desenvolvido como parte de um projeto acadêmico. O objetivo é demonstrar a viabilidade de classificar textos que expressam emoções, simulando um cenário de "previsão de crises de ansiedade" para uma aplicação de bem-estar.

O projeto utiliza o modelo leve `NeuroBERT-Tiny`, ideal para dispositivos móveis, e implementa uma técnica de **fine-tuning em duas etapas** para especializar e personalizar o modelo.

---

### Tecnologias e Técnicas Utilizadas

* **Linguagem:** Python
* **Frameworks:** PyTorch, Hugging Face Transformers
* **Modelo Base:** `boltuix/NeuroBERT-Tiny`
* **Dataset:** `dair-ai/emotion` (dados reais de emoções textuais)
* **Técnica Principal:** Fine-Tuning em duas etapas (Geral e Simulação por Usuário) com um loop de treinamento manual em PyTorch.

---

### Como Funciona

1.  **Preparação dos Dados:** O dataset `emotion`, com 6 classes de emoções, foi mapeado para 2 classes binárias: "Crise" (tristeza, raiva, medo) e "Normal" (alegria, amor, surpresa).
2.  **Fine-Tuning Geral:** O modelo `NeuroBERT-Tiny` foi treinado com 4.000 amostras para se tornar um especialista em classificar essas emoções.
3.  **Fine-Tuning por Usuário (Simulação):** O modelo especialista foi então submetido a um segundo treinamento com 50 amostras, simulando a personalização para o estilo de escrita de um único usuário.

O notebook (`.ipynb`) neste repositório contém o código completo e comentado de todo o processo.
