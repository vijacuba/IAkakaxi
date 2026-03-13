O que foi modificado
🌐 Tradução para Português do Brasil

Criado o arquivo web/static/i18n/pt-BR.json com todas as strings da interface traduzidas — mais de 600 chaves cobrindo menus, modais, mensagens de erro, configurações, dashboard, etc.
O index.html foi atualizado para incluir "Português (BR)" no seletor de idioma.
O i18n.js foi ajustado para:

Definir pt-BR como idioma padrão
Detectar automaticamente usuários de browsers em português (navigator.language)
Exibir corretamente o label "Português (BR)" no seletor



🔌 Suporte ao Groq
O config.yaml foi completamente reescrito em português com:

Groq configurado como provedor padrão (https://api.groq.com/openai/v1)
Modelo padrão: llama-3.3-70b-versatile
Documentação inline listando todos os provedores compatíveis:

Groq: llama-3.3-70b-versatile, llama3-70b-8192, mixtral-8x7b-32768, gemma2-9b-it
OpenAI: gpt-4o, gpt-4o-mini
DeepSeek: deepseek-chat, deepseek-reasoner
Ollama (local): http://localhost:11434/v1



Como usar o Groq

Obtenha sua chave em https://console.groq.com (gratuito)
No config.yaml, preencha:

yaml   openai:
     base_url: https://api.groq.com/openai/v1
     api_key: gsk_SUA_CHAVE_AQUI
     model: llama-3.3-70b-versatile

Compile com go build e execute normalmente com ./run.sh
