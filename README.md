# A Física Estatística do *Grokking*: Uma Abordagem Pedagógica do Aprendizado de Máquina

Este repositório contém os códigos-fonte, simulações e o manuscrito científico associados ao artigo **"A Física Estatística do *Grokking*: Uma Abordagem Pedagógica do Aprendizado de Máquina"**. 

O objetivo deste projeto é fornecer um material didático e reprodutível que ilustra o fenômeno de ***grokking*** (generalização tardia e abrupta em redes neurais) sob a perspectiva da Física Estatística e da Termodinâmica de sistemas desordenados, conectando conceitos de Deep Learning a fenômenos como transições de fase de primeira ordem, energia livre de Helmholtz, entropia e quebra espontânea de simetria.

---

## 📂 Estrutura do Repositório

O repositório está organizado da seguinte forma:

```text
├── notebooks/
│   ├── 01_mlp_grokking.ipynb              # Treinamento do MLP na tarefa de Aritmética Modular (a + b mod p)
│   ├── 02_transformer_grokking.ipynb      # Treinamento do mini-Transformer na Aritmética Modular (a + b mod p)
│   ├── 03_sparse_parity.ipynb             # MLP no problema da Paridade Esparsa (Sparse Parity) com ruído
│   ├── 04_sparse_parity_transformer.ipynb # Transformer no problema da Paridade Esparsa (Sparse Parity)
│   └── 05_modular_energy_conservation.ipynb# MLP e Transformer na Conservação de Energia Modular (x² + y² mod p)
├── paper/
│   ├── artigo_grokking.tex                # Arquivo fonte do artigo em LaTeX
│   ├── artigo_grokking.md                 # Arquivo fonte do artigo em Markdown
│   ├── artigo_grokking.pdf                # Artigo completo compilado em formato PDF
│   └── *.png                              # Gráficos e visualizações geradas pelas simulações
├── requirements.txt                       # Dependências do Python
└── README.md                              # Este arquivo de documentação
```

---

## 🚀 Como Executar as Simulações Localmente

### Pré-requisitos
Certifique-se de ter o Python 3.8+ instalado em sua máquina.

### 1. Clonar o Repositório
```bash
git clone https://github.com/jsansao/grokking.git
cd grokking
```

### 2. Criar e Ativar um Ambiente Virtual (Recomendado)
No Linux/macOS:
```bash
python3 -m venv venv
source venv/bin/activate
```
No Windows:
```cmd
python -m venv venv
venv\Scripts\activate
```

### 3. Instalar as Dependências
```bash
pip install -r requirements.txt
```

### 4. Iniciar o Jupyter Notebook
```bash
jupyter notebook
```
Uma janela do navegador será aberta. Navegue até a pasta `notebooks/` e execute os experimentos passo a passo. Todos os notebooks foram desenvolvidos para rodar rapidamente em CPU convencional, levando poucos minutos para atingir a convergência e gerar os gráficos.

---

## 🧠 Conceitos Físicos Explorados nos Notebooks

*   **Mapeamento Termodinâmico:** Mapeamento matemático entre os parâmetros da rede e um sistema mecânico-estatístico clássico:
    *   *Função de Perda* ($L_{\text{dados}}(w)$) $\leftrightarrow$ Energia Potencial de Interação com o conjunto de dados.
    *   *Decaimento de Pesos* (*Weight Decay*, $\lambda$) $\leftrightarrow$ Potencial Harmônico Restritivo (mola sináptica).
    *   *Dinâmica do Otimizador AdamW* $\leftrightarrow$ Equação de Langevin com temperatura efetiva.
*   **Transição de Fase Dinâmica:** Demonstração visual de como a acurácia de validação atua como um *parâmetro de ordem* que transiciona abruptamente de um estado de memorização desordenado (alta entropia e volume de parâmetros) para um estado generalizador ordenado (baixa energia/norma $L_2$).
*   **Cristalização Trigonométrica (Análise de Fourier):** Análise espectral de Fourier sobre os pesos da camada de *embedding* mostrando que o modelo aprende a aritmética modular ao alinhar periodicamente seus pesos na forma de senos e cossenos (invariância translacional no grupo cíclico $C_p$).
*   **Órbitas e Degenerescência no Espaço Latente:** Visualização em 2D (via PCA) do colapso de estados degenerados de energia (pares $x$ e $p-x$) e da auto-organização dos resíduos quadráticos em órbitas circulares concêntricas concêntricas sob o efeito do decaimento de pesos.

---

## 📄 O Artigo Científico

O manuscrito completo do artigo está disponível na pasta `paper/` em formato PDF:
*   👉 **[Acesse o PDF do Artigo](paper/artigo_grokking.pdf)**

Se você achar este material útil para suas aulas, estudos ou pesquisas, sinta-se à vontade para citar nosso trabalho:

```bibtex
@article{sansao2026grokking,
  title={A Física Estatística do Grokking: Uma Abordagem Pedagógica do Aprendizado de Máquina},
  author={Sansão, João Pedro Hallack},
  journal={Revista Brasileira de Ensino de Física},
  year={2026},
  volume={48},
  pages={e20250183},
  url={https://github.com/jsansao/grokking}
}
```

---

## ✉️ Contato e Suporte

**Autor:** Prof. João Pedro Hallack Sansão  
*Universidade Federal de São João del-Rei (UFSJ)*  
*Departamento de Tecnologia em Engenharia Civil, Computação, Automação, Telemática e Humanidades (DTECH)*  
📧 Email: `joao@ufsj.edu.br`  

Se encontrar algum problema nos códigos ou tiver sugestões pedagógicas, sinta-se à vontade para abrir uma *Issue* ou enviar um *Pull Request*!
