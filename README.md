<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Changelog – Tradução PT‑BR + Groq</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #050816;
      --bg-alt: #0b1020;
      --card: #111827;
      --accent: #22c55e;
      --accent-soft: rgba(34,197,94,0.12);
      --accent-2: #38bdf8;
      --text: #e5e7eb;
      --muted: #9ca3af;
      --border: rgba(148,163,184,0.4);
      --radius-lg: 14px;
      --radius-md: 10px;
      --shadow-soft: 0 18px 40px rgba(15,23,42,0.65);
      --mono: "Fira Code", ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      --sans: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: var(--sans);
      background: radial-gradient(circle at top, #1e293b 0, #020617 52%);
      color: var(--text);
      display: flex;
      justify-content: center;
      padding: 40px 16px;
    }

    .page {
      width: 100%;
      max-width: 960px;
      background: linear-gradient(145deg, rgba(15,23,42,0.96), rgba(15,23,42,0.98));
      border-radius: 22px;
      border: 1px solid rgba(148,163,184,0.45);
      box-shadow: var(--shadow-soft);
      padding: 28px 26px 32px;
      position: relative;
      overflow: hidden;
    }

    .page::before {
      content: "";
      position: absolute;
      inset: -40%;
      background:
        radial-gradient(circle at 0 0, rgba(56,189,248,0.14) 0, transparent 55%),
        radial-gradient(circle at 100% 0, rgba(52,211,153,0.12) 0, transparent 55%);
      opacity: .75;
      pointer-events: none;
      z-index: -1;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 16px;
      margin-bottom: 20px;
    }

    .title-block h1 {
      font-size: 1.6rem;
      letter-spacing: 0.02em;
      margin: 0 0 4px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .badge {
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      padding: 3px 10px;
      border-radius: 999px;
      border: 1px solid var(--border);
      color: var(--muted);
      background: rgba(15,23,42,0.9);
    }

    .subtitle {
      font-size: 0.9rem;
      color: var(--muted);
      margin: 0;
    }

    .meta {
      text-align: right;
      font-size: 0.78rem;
      color: var(--muted);
    }

    .meta strong {
      color: var(--accent-2);
      font-weight: 500;
    }

    h2 {
      font-size: 1.1rem;
      margin: 24px 0 10px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    h2 span.emoji {
      font-size: 1.3rem;
    }

    p {
      margin: 4px 0 10px;
      line-height: 1.55;
    }

    ul {
      margin: 6px 0 14px 1.05rem;
      padding: 0;
      color: var(--text);
    }

    li {
      margin-bottom: 4px;
    }

    .pill {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 2px 9px;
      border-radius: 999px;
      background: rgba(15,23,42,0.9);
      border: 1px solid var(--border);
      font-size: 0.75rem;
      color: var(--muted);
    }

    code, pre {
      font-family: var(--mono);
      font-size: 0.86rem;
    }

    code {
      padding: 1px 5px;
      border-radius: 6px;
      background: rgba(15,23,42,0.9);
      border: 1px solid rgba(51,65,85,0.9);
      color: #e5e7eb;
    }

    pre {
      margin: 10px 0 14px;
      padding: 12px 14px;
      border-radius: var(--radius-md);
      background: #020617;
      border: 1px solid rgba(51,65,85,0.95);
      overflow-x: auto;
      position: relative;
    }

    pre::before {
      content: "yaml";
      position: absolute;
      top: 6px;
      right: 10px;
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--muted);
      background: rgba(15,23,42,0.9);
      padding: 2px 6px;
      border-radius: 999px;
      border: 1px solid rgba(51,65,85,0.9);
    }

    a {
      color: var(--accent-2);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    .callout {
      margin-top: 14px;
      padding: 10px 12px;
      border-radius: var(--radius-md);
      border: 1px dashed rgba(148,163,184,0.8);
      background: radial-gradient(circle at 0 0, var(--accent-soft) 0, transparent 60%);
      font-size: 0.86rem;
      color: var(--muted);
    }

    .badge-strip {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 6px;
    }

    .badge-strip .stack {
      font-size: 0.75rem;
      padding: 2px 8px;
      border-radius: 999px;
      background: rgba(15,23,42,0.94);
      border: 1px solid rgba(55,65,81,0.9);
      color: var(--muted);
    }

    @media (max-width: 640px) {
      .page {
        padding: 20px 16px 22px;
        border-radius: 18px;
      }
      header {
        flex-direction: column;
        align-items: flex-start;
      }
      .meta {
        text-align: left;
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <header>
      <div class="title-block">
        <div class="badge">Changelog</div>
        <h1>
          Tradução PT‑BR + Suporte ao Groq
        </h1>
        <p class="subtitle">
          Atualizações de internacionalização da interface web e configuração de provedores LLM.
        </p>
        <div class="badge-strip">
          <span class="stack">i18n</span>
          <span class="stack">frontend</span>
          <span class="stack">config.yaml</span>
        </div>
      </div>
      <div class="meta">
        <div>Idioma padrão: <strong>Português (BR)</strong></div>
        <div>Modelo default: <strong>llama-3.3-70b-versatile</strong></div>
      </div>
    </header>

    <section>
      <h2><span class="emoji">🛠️</span> O que foi modificado</h2>
    </section>

    <section>
      <h2><span class="emoji">🌐</span> Tradução para Português do Brasil</h2>
      <p>
        Toda a interface foi traduzida para <strong>Português do Brasil</strong>, cobrindo menus, modais,
        mensagens de erro, configurações, dashboards e mais.
      </p>
      <ul>
        <li>
          Criado o arquivo
          <code>web/static/i18n/pt-BR.json</code>
          com <strong>600+ chaves</strong> traduzidas.
        </li>
        <li>
          <code>index.html</code> atualizado para incluir
          <code>Português (BR)</code> no seletor de idioma.
        </li>
        <li>
          <code>i18n.js</code> ajustado para:
          <ul>
            <li>Definir <code>pt-BR</code> como idioma padrão.</li>
            <li>Detectar automaticamente browsers em português via <code>navigator.language</code>.</li>
            <li>Exibir o label <code>Português (BR)</code> corretamente no seletor.</li>
          </ul>
        </li>
      </ul>
    </section>

    <section>
      <h2><span class="emoji">🔌</span> Suporte ao Groq</h2>
      <p>
        O arquivo <code>config.yaml</code> foi reescrito em português, com o
        <strong>Groq configurado como provedor padrão</strong> usando o endpoint
        <code>https://api.groq.com/openai/v1</code>.
      </p>
      <ul>
        <li>Modelo padrão: <code>llama-3.3-70b-versatile</code>.</li>
        <li>Documentação inline listando provedores compatíveis:
          <ul>
            <li><strong>Groq</strong>:
              <code>llama-3.3-70b-versatile</code>,
              <code>llama3-70b-8192</code>,
              <code>mixtral-8x7b-32768</code>,
              <code>gemma2-9b-it</code>
            </li>
            <li><strong>OpenAI</strong>: <code>gpt-4o</code>, <code>gpt-4o-mini</code></li>
            <li><strong>DeepSeek</strong>: <code>deepseek-chat</code>, <code>deepseek-reasoner</code></li>
            <li><strong>Ollama (local)</strong>: <code>http://localhost:11434/v1</code></li>
          </ul>
        </li>
      </ul>
    </section>

    <section>
      <h2><span class="emoji">🚀</span> Como usar o Groq</h2>
      <ol>
        <li>
          Obtenha sua chave em
          <a href="https://console.groq.com" target="_blank" rel="noreferrer">
            https://console.groq.com
          </a>
          (plano gratuito disponível).
        </li>
        <li>No arquivo <code>config.yaml</code>, preencha a seção do provedor:</li>
      </ol>

      <pre><code>openai:
  base_url: https://api.groq.com/openai/v1
  api_key: gsk_SUA_CHAVE_AQUI
  model: llama-3.3-70b-versatile</code></pre>

      <ol start="3">
        <li>Compile o binário com <code>go build</code>.</li>
        <li>Execute normalmente com <code>./run.sh</code>.</li>
      </ol>

      <div class="callout">
        Dica: mantenha diferentes perfis de <code>config.yaml</code> (Groq, OpenAI, Ollama)
        versionados em arquivos separados e use variáveis de ambiente ou flags
        para alternar entre provedores em desenvolvimento vs. produção.
      </div>
    </section>
  </main>
</body>
</html>
