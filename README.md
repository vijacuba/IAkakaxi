## 🛠️ O que foi modificado

---

### 🌐 Tradução para Português do Brasil

Criado o arquivo `web/static/i18n/pt-BR.json` com todas as strings da interface traduzidas —
mais de **600 chaves** cobrindo menus, modais, mensagens de erro, configurações, dashboard, etc.

- `index.html` atualizado para incluir **"Português (BR)"** no seletor de idioma.
- `i18n.js` ajustado para:
  - Definir `pt-BR` como idioma padrão
  - Detectar automaticamente usuários de browsers em português (`navigator.language`)
  - Exibir corretamente o label **"Português (BR)"** no seletor

---

### 🔌 Suporte ao Groq

O `config.yaml` foi completamente reescrito em português com:

- **Groq** configurado como provedor padrão (`https://api.groq.com/openai/v1`)
- Modelo padrão: `llama-3.3-70b-versatile`
- Documentação inline listando todos os provedores compatíveis:

| Provedor | Modelos disponíveis |
|---|---|
| **Groq** | `llama-3.3-70b-versatile`, `llama3-70b-8192`, `mixtral-8x7b-32768`, `gemma2-9b-it` |
| **OpenAI** | `gpt-4o`, `gpt-4o-mini` |
| **DeepSeek** | `deepseek-chat`, `deepseek-reasoner` |
| **Ollama (local)** | `http://localhost:11434/v1` |

---

### 🚀 Como usar o Groq

1. Obtenha sua chave em [https://console.groq.com](https://console.groq.com) *(plano gratuito disponível)*
2. No `config.yaml`, preencha:

```yaml
openai:
  base_url: https://api.groq.com/openai/v1
  api_key: gsk_SUA_CHAVE_AQUI
  model: llama-3.3-70b-versatile
