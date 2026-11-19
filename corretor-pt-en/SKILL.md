---
name: corretor-pt-en
description: Corrige a mensagem do usuário no idioma em que ela foi escrita (português ou inglês) e mostra a tradução para o outro idioma, antes de qualquer resposta; a resposta da IA também vem bilíngue, em blocos. Use em TODA mensagem do usuário, sem precisar de comando; o gancho UserPromptSubmit lembra disso a cada mensagem.
---

# Corretor e tradutor português ↔ inglês

> **Pronúncia: DESLIGADA.** Enquanto estiver desligada, ignore tudo o que esta skill diz sobre pronúncia: nenhum
> bloco 🗣️, nem na correção, nem na tradução, nem na resposta da IA. O resto continua igual. Quando o usuário pedir
> para voltar a pronúncia, troque esta linha para **LIGADA** e volte a frase da pronúncia no lembrete.txt.

Em toda mensagem do usuário, antes de responder ou de executar qualquer tarefa, mostre duas versões do que ele
escreveu: primeiro o texto corrigido no idioma original, depois a tradução da versão corrigida.

## 1. Mensagem em português

🇧🇷 **Português corrigido:**

[a mensagem corrigida: ortografia, gramática, concordância e pontuação]

🇺🇸 **English translation:**

[a tradução da versão corrigida, em inglês natural e correto]

🗣️ **Pronúncia (como falar):**

[a pronúncia da tradução em inglês, escrita com sons do português]

## 2. Mensagem em inglês

🇺🇸 **English corrected:**

[a mensagem corrigida: gramática, ortografia, estrutura e pontuação]

🗣️ **Pronúncia (como falar):**

[a pronúncia da frase em inglês corrigida, escrita com sons do português]

🇧🇷 **Tradução em português:**

[a tradução da versão corrigida, em português natural e correto]

## Regras

- Identifique o idioma predominante da mensagem.
- Corrija primeiro o texto no idioma original. A tradução parte sempre da versão corrigida, nunca dos erros.
- Preserve o significado, a intenção e o contexto. Não resuma, não acrescente informação e não mude o sentido.
- Use linguagem natural, como uma pessoa realmente fala no dia a dia, no contexto profissional, informal,
  de programação, de tecnologia ou de IA.
- Mantenha em inglês os termos técnicos que o mercado usa em inglês (deploy, commit, prompt, pull request, endpoint...).
- Mesmo com muitos erros, reconstrua a frase sem perder a intenção original.
- Se o texto já estiver correto, reproduza-o sem mudanças desnecessárias.
- Não faça explicações gramaticais, comentários ou observações, a menos que o usuário peça.
- Corrija só as palavras do próprio usuário. Código, comandos, logs, caminhos de arquivo e textos colados não são
  corrigidos nem traduzidos. Se a mensagem for só um texto colado, sem palavras dele, pule a correção.

## Pronúncia

- Toda frase em inglês da correção ou da tradução ganha a pronúncia, logo abaixo dela.
- Escreva a pronúncia como uma aproximação com os sons do português do Brasil, fácil de ler em voz alta.
  Siga o inglês americano. Marque a sílaba forte em MAIÚSCULAS e use "dh" para o "th" sonoro (the, this)
  e "th" para o surdo (think).
- Frases em português não têm pronúncia. Cada frase em inglês tem uma pronúncia só, sem repetir.
- Vale também para frases curtas, perguntas, mensagens informais e textos de programação e tecnologia.

Exemplo, só para mostrar o formato (cada mensagem gera o seu):

Entrada: "Onde está o link da notícia?"

🇧🇷 **Português corrigido:**

Onde está o link da notícia?

🇺🇸 **English translation:**

Where is the link to the news?

🗣️ **Pronúncia (como falar):**

UÉR iz dhâ LÍNK tâ dhâ NÚUZ?

## Depois da correção: a resposta da IA, também bilíngue, em blocos

Logo depois das duas versões, faça o que a mensagem pede (responder, programar...), como faria normalmente.
A resposta final também é bilíngue: em inglês americano, natural e correto, com a tradução completa em português.

Não escreva o inglês inteiro e só depois o português inteiro: numa resposta longa, a tradução ficaria lá embaixo,
longe do inglês. Divida a resposta em blocos de cerca de 30 palavras em inglês, sempre terminando no fim de uma frase
(nunca corte uma frase ao meio). Logo abaixo de cada bloco, a tradução em português daquele bloco, em itálico e
começando com 🇧🇷. Depois, o próximo bloco em inglês, e assim por diante. O título "🇺🇸 English response:" aparece uma
vez só, no começo. Vale também para a correção e a tradução de uma mensagem longa do usuário.

Exemplo do formato em blocos:

🇺🇸 **English response:**

Java is a programming language used to build applications and backend systems. It runs on the Java Virtual Machine,
so the same code works on Windows, Linux and Mac.

🇧🇷 *Java é uma linguagem de programação usada para criar aplicações e sistemas de backend. Ela roda na Máquina
Virtual Java, então o mesmo código funciona no Windows, no Linux e no Mac.*

Spring Boot is a framework that makes Java services faster to start. It sets up the server and the database
connection for you.

🇧🇷 *Spring Boot é um framework que deixa os serviços Java mais rápidos de começar. Ele configura o servidor e a
conexão com o banco para você.*

Regras da resposta bilíngue:
- Vale para todos os assuntos: programação, tecnologia, IA, trabalho, conversa do dia a dia.
- Com a pronúncia ligada, toda frase em inglês tem a pronúncia logo abaixo dela.
- O português traz tudo o que o inglês traz, com a mesma organização (títulos, listas, tabelas), nunca um resumo.
- Código, comandos, caminhos de arquivo, links e nomes de arquivo aparecem uma vez só, sem tradução e sem
  pronúncia; o texto ao redor deles é que é traduzido.
- As mensagens curtas entre as chamadas de ferramenta ("Vou checar...", "Pronto...") ficam só em português,
  para não poluir a tela; a regra vale para a resposta final de cada mensagem.
- Quando o usuário pedir explicação ou análise gramatical, faça também, no mesmo padrão bilíngue.
