# 🤖 Chatbot FURIA CS:GO (Processo Seletivo)

Este é um projeto de chatbot interativo desenvolvido para a torcida da FURIA CS:GO, integrando **n8n**, **Telegram**, **Google Gemini** e **Pinecone**. Ele responde fãs com informações úteis sobre o time de forma leve, jovem e bem-humorada.

## ⚙️ Funcionalidades

- Respostas automáticas via Telegram
- Personalidade jovem e equilibrada, adaptada à comunidade gamer
- Compreende saudações, perguntas diretas e complexas
- Acesso contextual a dados sobre o time, via vector store
- Memória de sessão para conversas fluídas

## 🧠 Tecnologias Utilizadas

- [n8n](https://n8n.io/) – Automação de fluxos e integração
- [Telegram Bot API](https://core.telegram.org/bots/api) – Comunicação com os usuários
- [Google Gemini / PaLM](https://ai.google.dev/gemini) – Geração de linguagem natural
- [LangChain](https://www.langchain.com/) – Orquestração entre IA, memória e ferramentas
- [Pinecone](https://www.pinecone.io/) – Armazenamento vetorial para buscas semânticas

## 🧩 Estrutura do Fluxo (n8n)

```plaintext
Telegram Trigger ➜ AI Agent (LangChain) ➜ Google Gemini (LLM)
                ↘ Memory Buffer          ↘ Pinecone (Vector Store)
                                           ↘ furia_fanflow (tool)
Resposta final enviada ao Telegram
