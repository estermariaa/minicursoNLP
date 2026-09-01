## O que é NLP
	Subcampo da IA focada na interação entre computadores e linguagem humana

O Processamento de Linguagem Natural (ou _Natural Language Processing_, NLP) é uma área central da Inteligência Artificial que busca permitir que computadores entendam, gerem e interajam com a linguagem humana de forma automatizada. Ele integra conhecimentos de linguística, estatística, aprendizado de máquina e deep learning para resolver tarefas complexas, como análise de sentimentos, tradução, classificação de textos, entre outras.

Transformação de dados não estruturados em dados estruturados

Leitura de texto
Geração de texto

## Material Suplementar

[ What is NLP (Natural Language Processing)?](https://www.youtube.com/watch?v=fLvJ8VdHLA0)
[PLN: Respondendo à Linguagem Humana - @CursoemVideo Inteligência Artificial](https://www.youtube.com/watch?v=FTZuA31dbwk)
[Artigo Medium](https://medium.com/@bruno.facco/processamento-de-linguagem-natural-principais-conceitos-e-aplica%C3%A7%C3%B5es-0b2d0be30933)
https://github.com/iAmKankan/Natural-Language-Processing-NLP-Tutorial#natural-language-processing-nlp
https://portaldelivros.ufg.br/index.php/cegrafufg/catalog/book/649
https://huggingface.co/learn/llm-course/chapter1/3
## Objetivo

Permitir que máquinas entendem, interpretem e respondam à linguagem humana de uma maneira que seja tanto valiosa quanto significativa.

Busca construir pontes entre máquinas e humanos através da linguagem, tornando possível a comunicação fluida e a extração de informações valiosas dos textos.

LER OUVIR E FALAR
## Principais Aplicações

|Information Retrieval|Find documents based on keywords|
|:--|:--|
|Information Extraction|Identify and extract personal name, date, company name, city..|
|Language generation|Description based on a photograph, Title for a photograph|
|Text classification|Assigning predefined categorization to documents. Identify Spam emails and move them to a Spam folder|
|Machine Translation|Translate any language Text to another|
|Grammar checkers|Check the grammar for any language

### 2.1 Classificação de Texto
Dividir textos em categorias: **spam vs. não-spam**, classificação de notícias (esporte, política, entretenimento), classificação de e-mails corporativos etc. Modelos como _Naive Bayes_ e _Logistic Regression_ são muito utilizados, mas para tarefas mais complexas, _transformers_ podem oferecer maior acurácia.
### 2.2 Análise de Sentimentos
Avalia o tom emocional de um texto (positivo, negativo ou neutro). Muito usado no **monitoramento de redes sociais**, feedback de produtos, pesquisas de opinião, etc.

- **Exemplo**: “O produto é excelente!” → positivo.
- **Exemplo**: “O suporte demorou muito a responder” → negativo.
### 2.3 Tradução Automática
Sistemas de **tradução automática** (ex.: Google Translate) buscam transformar textos de um idioma para outro. Modelos _seq2seq_ baseados em **transformers** (como o MarianMT) dominam atualmente.
### 2.4 Chatbots e Assistentes Virtuais
Siri, Alexa e Google Assistant são exemplos populares de chatbots que precisam compreender intenções, extrair entidades e gerar respostas coerentes.

### 2.5 Extração de Informação (Information Extraction)
Identifica e extrai dados estruturados de textos não estruturados. Em **Reconhecimento de Entidades Nomeadas (NER)**, por exemplo, encontramos nomes de pessoas, organizações, localizações, etc.

### 2.6 Resumo Automático de Textos (Text Summarization)
Cria resumos concisos de textos longos. **Abordagens extrativas** selecionam frases importantes do texto original, enquanto **abordagens abstrativas** geram novas frases de forma semelhante a como um humano faria.

Recomendacao modelagem de topicos e classificacao

Entendimento de texto - saídas diferentes

Machine translation
Virtual assistent (chatbot)
Sentiment analysis
Spam detection
resumos automaticos

Entendimento e geração de texto
Siri Alexa (Voz - texto)
LLMS (GTP, Gemini, Clause)
## 1. Principais Conceitos

### 1.1 Tokenização (_Tokenization_)

A **tokenização** é o processo de dividir um texto em unidades menores, chamadas _tokens_. Geralmente, essas unidades correspondem a palavras, mas dependendo da abordagem podem ser subpalavras (como no BPE — _Byte Pair Encoding_) ou até mesmo caracteres (muito comum em línguas asiáticas).

### Por que tokenizar?

1. **Facilita a análise estatística**: algoritmos de NLP operam em cadeias de _tokens_ ao invés de cadeias de caracteres brutos.
2. **Reduz ruídos**: pontuações e outros caracteres especiais podem ser isolados, permitindo limpeza mais fácil.

### 1.2 Normalização e Limpeza de Dados (Text Preprocessing)
- #### **1.2.1. Remoção de pontuação**
- #### **1.2.2. Conversão para minúsculas**
- #### **1.2.3. Remoção de _stopwords_**
- #### **1.2.4. Stemming**
- #### **1.2.5. Lematização**

### 1.3 Representação de Textos (Text Representation)

Após tokenizar e limpar os textos, precisamos convertê-los em **vetores numéricos**, pois modelos de Aprendizado de Máquina e _Deep Learning_ só entendem números. 

O Trivial é transformar cada palavra em um número diferente, porém essa técnica, por mais eficiente que seja, não é capaz de carregar significado para o modelo posterior. O objetivo da representação é levar o máximo do conhecimento textual para os número

- #### 1.3.1 Bag-of-Words (BoW)
Na técnica de **Bag-of-Words**, cada documento (texto) é representado por um vetor que conta a frequência de cada palavra do vocabulário. Suponha que tenhamos um vocabulário de V palavras. Cada documento d torna-se um vetor x ∈ R^V, onde cada componente xi é o número de ocorrências da i-ésima palavra nesse documento.
Mais tempo nisso

- ### 1.3.2 TF-IDF (Term Frequency — Inverse Document Frequency)

- ### 1.3.3 Word Embeddings
Ao contrário das representações esparsas (BoW, TF-IDF), **word embeddings** são representações densas em vetores de dimensão fixa (ex.: 100 ou 300 dimensões). Técnicas como **Word2Vec**, **GloVe** e **FastText** aprenderam, de forma não supervisionada, vetores que capturam semântica: palavras parecidas semanticamente ficam próximas no espaço vetorial.

### **Exemplo**:

Se v(“rei”) é o vetor para “rei” e v(“homem”) para “homem”, e v(“mulher”) para “mulher”, então:
v(“rei”) − v(“homem”) + v(“mulher”) ≈ v(“rainha”)

### 1.3.4 Contextual Embeddings (Transformers)

Modelos mais recentes, como **BERT**, **GPT**, **RoBERTa**, entre outros, produzem **embeddings contextuais**, ou seja, a representação de uma palavra varia conforme o contexto em que ela aparece. Isso ajuda a lidar com problemas de polissemia, pois “banco” em “sentar no banco da praça” terá um embedding diferente de “banco” em “abrir uma conta em um banco”.

### 1.4 Modelos de Linguagem

Um **modelo de linguagem** estima a probabilidade de uma sequência de palavras (w1,w2,…,wn). Uma formulação clássica via _chain rule_ é:

![](https://miro.medium.com/v2/resize:fit:563/1*ltidqkDPMIM0ktxjiATRdA.png)

**Modelos baseados em _n_-gramas** aproximavam essa probabilidade considerando um histórico de tamanho fixo. Hoje, **transformers** revolucionaram os modelos de linguagem com mecanismos de _self-attention_ que capturam contexto global do texto.

### 1.5 Técnicas de Aprendizado
### **Modelos Tradicionais**
- **Naive Bayes**
- **KNN**
- **SVM (Support Vector Machines)**
- **Random Forest** 
- **Regressão Logística**

N.E.R