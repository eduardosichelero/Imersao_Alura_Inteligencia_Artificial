# Explicação do Código

Este código demonstra como usar o Google Gemini Pro para gerar texto e interagir em um chat.

## Funcionalidades

- **Instalação e configuração:**
  - Instala o SDK do Google Generative AI.
  - Importa a biblioteca `google.generativeai`.
  - Configura a chave de API do Google (substitua `YOUR_API_KEY` pela sua chave).

- **Listagem de modelos:**
  - Lista os modelos disponíveis para geração de conteúdo.

- **Configurações:**
  - Define configurações para a geração de texto, como `candidate_count` (número de candidatos) e `temperature` (criatividade).
  - Define configurações de segurança (desabilitadas neste exemplo para fins de demonstração).

- **Geração de texto simples:**
  - Usa o modelo `gemini-1.0-pro` para gerar uma resposta à pergunta "Que empresa criou o modelo de IA Gemini?".

- **Chat interativo:**
  - Inicia um chat com o modelo `gemini-1.0-pro`.
  - Permite ao usuário digitar prompts e receber respostas do modelo.
  - O chat continua até que o usuário digite "fim".

- **Formatação do histórico do chat:**
  - Usa HTML, Markdown e JavaScript para formatar o histórico do chat como cartões visuais, com cores diferentes para o usuário e o BOT.
  - Inclui a funcionalidade de copiar a resposta do BOT para a área de transferência.
