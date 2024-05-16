# Explicação do Código

Este código demonstra como usar o Google Gemini Pro para gerar embeddings e realizar buscas semânticas em documentos.

## Funcionalidades

- **Instalação e configuração:**
  - Instala o SDK do Google Generative AI.
  - Importa as bibliotecas `numpy`, `pandas` e `google.generativeai`.
  - Configura a chave de API do Google (substitua `YOUR_API_KEY` pela sua chave).

- **Listagem de modelos:**
  - Lista os modelos disponíveis para embedding.

- **Exemplo de embedding:**
  - Gera embeddings para um texto de exemplo usando o modelo `models/embedding-001`.

- **Criação do conjunto de dados:**
  - Define três documentos de exemplo com títulos e conteúdos.
  - Cria um DataFrame pandas com os documentos.

- **Geração de embeddings para os documentos:**
  - Define uma função `embed_fn` para gerar embeddings para um título e texto.
  - Aplica a função `embed_fn` a cada linha do DataFrame para gerar embeddings para cada documento.
  - Adiciona os embeddings como uma nova coluna no DataFrame.

- **Busca semântica:**
  - Define uma função `gerar_e_buscar_consulta` que:
    - Gera embeddings para a consulta do usuário.
    - Calcula o produto escalar entre os embeddings da consulta e dos documentos.
    - Encontra o índice do documento com o maior produto escalar (ou seja, o documento mais semanticamente similar à consulta).
    - Retorna o conteúdo do documento mais relevante.

- **Reescrita de texto:**
  - Define um prompt para reescrever o trecho encontrado de forma mais descontraída.
  - Usa o modelo `gemini-1.0-pro` com configurações de baixa criatividade para reescrever o texto sem adicionar novas informações.
