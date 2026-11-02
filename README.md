# Assistente com IA (PWA)

App de celular com comando de voz e agentes que aprendem com o seu dia a dia.
Ao abrir, ele pergunta se você precisa de ajuda.

## Como usar no celular

O microfone exige HTTPS (ou localhost). Opções:

1. **Teste rápido no PC:** na pasta `versao`, rode `npx serve .` e abra `http://localhost:3000`.
2. **No celular:** publique a pasta `versao` em um host HTTPS gratuito (GitHub Pages, Netlify, Cloudflare Pages), abra o link no **Chrome do Android** e use **Menu > Adicionar à tela inicial**. Ele passa a abrir como app.

## Comandos de voz

- "tarefa comprar café" / "preciso pagar a conta de luz"
- "estou estudando inglês" ... "terminei"
- "concluir café"
- "minhas tarefas", "resumo do dia", "sugestões", "ajuda"

## Agentes (aprendem sozinhos, tudo salvo só no seu aparelho)

| Agente | O que aprende | O que sugere |
|---|---|---|
| Rotina | Atividades repetidas no mesmo horário (3+ dias) | Criar rotina e te avisar ao abrir o app |
| Foco | Acúmulo de tarefas e tarefas paradas | Priorizar 3 e dividir em primeiro passo |
| Hábitos | Sessões longas (90+ min) | Pausas regulares |
| Comandos | Frases que você repete e o app não entendeu | Salvar como atalho |

Use o botão **Carregar exemplo de uso** na aba Agentes para ver tudo funcionando de imediato.

## Próximos passos (se quiser IA generativa de verdade)

Hoje os agentes usam regras locais, sem enviar nada para fora. Para conversa livre e sugestões mais inteligentes, o caminho é criar um pequeno backend que chama a API do Claude (a chave nunca deve ficar no app) e enviar a ele o resumo das atividades. Também dá para empacotar o PWA como app nativo (Capacitor) para ter notificações em segundo plano.
