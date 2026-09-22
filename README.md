# Testador de Prompts — Digital Moon

Ambiente para testar prompts de pré-atendimento (SDR/comercial) como se fossem
uma conversa real de WhatsApp: as respostas da IA chegam quebradas em várias
mensagens, com pausa e "digitando…" simulados, para avaliar o ritmo real que
um lead sentiria.

## Como usar

Não tem build, nem backend — é uma página só (`index.html`).

**Opção 1 — abrir local:**
```
git clone https://github.com/contato609/testadordeprompt.git
cd testadordeprompt
open index.html   # ou dois cliques no arquivo
```

**Opção 2 — GitHub Pages:** em Settings → Pages deste repositório, publique a
branch `main` (pasta raiz) e a ferramenta fica disponível numa URL pública
para o time inteiro usar, sem precisar baixar nada.

## Funcionalidades

- **Biblioteca de prompts** — salve, duplique e edite quantos prompts/agentes
  quiser. Cada um guarda sua própria conversa de teste (tudo no
  `localStorage` do navegador de quem está usando).
- **Conexão com a OpenAI** — cada pessoa cola a própria API key no painel
  "Conexão com a IA". A key fica só no navegador local; nada é enviado a
  nenhum servidor além da própria API da OpenAI.
- **Ritmo de digitação** — a resposta da IA é quebrada em várias mensagens
  (por linha em branco, quebra de linha simples, ou um marcador customizado
  ensinado no próprio prompt do sistema), cada bloco chega após uma pausa
  aleatória + bolha de "digitando…", com velocidade configurável.
- **Exportar conversa** — baixa um `.txt` com o prompt usado e o histórico
  de teste, para documentar ou compartilhar com o time.

## Segurança

A API key da OpenAI nunca sai do navegador de quem está testando — é usada
apenas para chamar `api.openai.com` diretamente do cliente. Não compartilhe
prints ou links desta página com a key preenchida.
