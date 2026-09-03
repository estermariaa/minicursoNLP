# Processamento de Linguagem Natural (NLP) — Guia de Estudos e Conceitos

## 1. O que é NLP?
Subcampo da Inteligência Artificial focado na interação entre computadores e linguagem humana. O Processamento de Linguagem Natural busca permitir que sistemas entendam, gerem e interajam com a linguagem de forma automatizada, integrando conhecimentos de linguística, estatística, aprendizado de máquina e deep learning para resolver tarefas complexas.

* **Objetivo Principal:** Construir pontes entre máquinas e humanos através da linguagem, permitindo a comunicação fluida, leitura, audição, fala, compreensão, interpretação e a extração de informações valiosas de dados textuais não estruturados.
* **Principais Desafios:** Transformação de dados não estruturados em dados estruturados, entendimento de texto com saídas diferentes, além da geração de texto.

---

## 2. Principais Aplicações

| Aplicação | Descrição / Objetivo |
| :--- | :--- |
| **Information Retrieval** | Encontrar documentos com base em palavras-chave. |
| **Information Extraction** | Identificar e extrair nomes de pessoas, datas, nomes de empresas, cidades, etc. (Inclui o Reconhecimento de Entidades Nomeadas — N.E.R). |
| **Language Generation** | Geração de descrições baseadas em fotografias, títulos para imagens, etc. |
| **Text Classification** | Atribuir categorizações predefinidas a documentos (ex: identificar e-mails de spam e movê-los para a pasta correspondente, divisão entre spam vs. não-spam, classificação de notícias e e-mails corporativos). |
| **Machine Translation** | Traduzir textos de qualquer idioma para outro. |
| **Grammar Checkers** | Verificar a gramática de qualquer idioma. |
| **Análise de Sentimentos** | Avaliar o tom emocional de um texto (positivo, negativo ou neutro) para monitoramento de redes sociais e feedback de produtos. |
| **Chatbots e Assistentes Virtuais** | Sistemas interativos (como Siri, Alexa e Google Assistant) que processam voz/texto, compreendem intenções e geram respostas coerentes. |
| **Resumo Automático de Textos** | Criação de sínteses de textos longos por meio de abordagens extrativas ou abstrativas. |

---

## 3. Principais Conceitos

### 3.1 Tokenização (*Tokenization*)
Processo de dividir o texto bruto em unidades menores chamadas *tokens* (geralmente palavras, mas podendo ser subpalavras como no BPE — *Byte Pair Encoding*, ou caracteres).
* **Por que tokenizar?** Facilita a análise estatística (pois algoritmos operam em cadeias de tokens e não em caracteres brutos) e reduz ruídos ao isolar pontuações.

### 3.2 Normalização e Limpeza de Dados (*Text Preprocessing*)
Etapas fundamentais para estruturar o texto:
* **Remoção de pontuação**
* **Conversão para minúsculas**
* **Remoção de *stopwords***
* **Stemming**
* **Lematização**

### 3.3 Representação de Textos (*Text Representation*)
Conversão de textos limpos em vetores numéricos para que algoritmos de Machine Learning e Deep Learning possam processá-los:
* **Bag-of-Words (BoW):** Representa cada documento por um vetor que conta a frequência de cada palavra de um vocabulário fixo $V$ ($x \in \mathbb{R}^V$).
* **TF-IDF (*Term Frequency — Inverse Document Frequency*):** Combina a frequência do termo no documento com a sua raridade global na base de dados.
* **Word Embeddings:** Vetores densos de dimensão fixa (ex: Word2Vec, GloVe, FastText) que capturam semelhanças semânticas (ex: $v(\text{"rei"}) - v(\text{"homem"}) + v(\text{"mulher"}) \approx v(\text{"rainha"})$).
* **Contextual Embeddings (Transformers):** Modelos como BERT, GPT e RoBERTa onde a representação da palavra varia conforme o contexto, resolvendo problemas de polissemia.

### 3.4 Modelos de Linguagem
Estimam a probabilidade de uma sequência de palavras ($w_1, w_2, \dots, w_n$). 
* Histórico de modelos baseados em *n*-gramas versus a revolução dos **Transformers** através de mecanismos de *self-attention* para capturar o contexto global.

### 3.5 Técnicas de Aprendizado
* **Modelos Tradicionais:** Naive Bayes, KNN, SVM (*Support Water Machines*), Random Forest e Regressão Logística.

---

## 4. Material Suplementar e Links Úteis

### 🎥 Vídeos e Aulas
* [What is NLP (Natural Language Processing)?](https://www.youtube.com/watch?v=fLvJ8VdHLA0) — Vídeo introdutório explicando os fundamentos de NLP.
* [PLN: Respondendo à Linguagem Humana - @CursoemVideo](https://www.youtube.com/watch?v=FTZuA31dbwk) — Aula prática abordando conceitos de Inteligência Artificial voltados a Processamento de Linguagem Natural.

### 📚 Artigos, Tutoriais e Documentações
* [Artigo Medium — Processamento de Linguagem Natural: Principais Conceitos e Aplicações](https://medium.com/@bruno.facco/processamento-de-linguagem-natural-principais-conceitos-e-aplica%C3%A7%C3%B5es-0b2d0be30933) — Texto explicativo cobrindo a teoria essencial da área.
* [Turing Talks — Ambientes Virtuais em Python](https://medium.com/turing-talks/ambientes-virtuais-em-python-60924a4bf4f) — Guia prático sobre o gerenciamento de dependências e ambientes virtuais para projetos de programação.
* [Hugging Face LLM Course (Chapter 1)](https://huggingface.co/learn/llm-course/chapter1/3) — Curso focado em modelos de linguagem de grande escala.
* [Scikit-learn: Decision Trees](https://scikit-learn.org/stable/modules/tree.html) — Documentação técnica oficial sobre algoritmos de Árvores de Decisão em Python.
* [Pandas Cheat Sheet for Data Science](https://datascientyst.com/pandas-cheat-sheet-for-data-science/) — Folha de consulta rápida com os comandos mais úteis da biblioteca Pandas.
* [Repositório GitHub (iAmKankan)](https://github.com/iAmKankan/) — Perfil contendo códigos, códigos de tutoriais e projetos práticos relacionados a ciência de dados e NLP.
* [Natural Language Processing NLP Tutorial](https://github.com/iAmKankan/Natural-Language-Processing-NLP-Tutorial) — Repositório com materiais práticos e tutoriais guiados de NLP.
* [Portal de Livros UFG](https://portaldelivros.ufg.br/index.php/cegrafufg/catalog/book/649) — Publicação acadêmica voltada a conteúdos editoriais e científicos da Universidade Federal de Goiás.