# corretor-pt-en

Uma skill para o [Claude Code](https://claude.com/claude-code) que transforma cada conversa em treino de inglês.

- **A sua mensagem**: o Claude corrige o que você escreveu (em português ou inglês) e mostra a tradução para o outro idioma.
- **A resposta do Claude**: vem em inglês, em blocos de cerca de 30 palavras, cada um com a tradução em português logo abaixo.
- **Pronúncia (opcional)**: cada frase em inglês pode ganhar a pronúncia escrita com sons do português
  (ex.: "UÉR iz dhâ LÍNK tâ dhâ NÚUZ?"). Vem desligada; peça "volta a pronúncia" para ligar.

## Exemplo

> 🇧🇷 **Português corrigido:** Onde está o link da notícia?
>
> 🇺🇸 **English translation:** Where is the link to the news?

## Instalação

1. Copie a pasta `corretor-pt-en/` para `~/.claude/skills/`.
2. Para valer em **toda** mensagem (uma skill sozinha só é usada quando o assunto combina com ela), adicione este
   gancho ao `~/.claude/settings.json`:

macOS / Linux:

```json
{
  "hooks": {
    "UserPromptSubmit": [
      { "hooks": [ { "type": "command", "command": "cat ~/.claude/skills/corretor-pt-en/lembrete.txt" } ] }
    ]
  }
}
```

Windows (PowerShell):

```json
{
  "hooks": {
    "UserPromptSubmit": [
      { "hooks": [ { "type": "command", "shell": "powershell",
        "command": "Get-Content -Raw \"$env:USERPROFILE\\.claude\\skills\\corretor-pt-en\\lembrete.txt\"" } ] }
    ]
  }
}
```

Se o seu `settings.json` já tiver uma seção `hooks`, junte o bloco `UserPromptSubmit` a ela.

3. Abra uma conversa nova no Claude Code.

## Ligar e desligar

- **Pronúncia**: peça "volta a pronúncia" ou "tira a pronúncia".
- **Tudo**: apague o bloco `UserPromptSubmit` do `settings.json`.

## Licença

MIT
