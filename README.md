# guerra-de-times

Cabo de guerra entre dois times pra live do TikTok. O chat escolhe um lado, comenta pra empurrar a linha de frente e quem levar o round ganha. Nome, cor, emoji, foto e comando de cada time são editáveis, e dá pra salvar presets (tipo Dexter × Mentalista). Layout vertical 9:16, arquivo único (`index.html`).

## Como joga

- O chat escolhe o time pelo comando, por exemplo `!dexter` ou `!mentalista`. `!1` e `!2` também funcionam. Quem só comenta cai no time menor.
- Comentário vale ponto, curtida dá turbo e presente dá um empurrão grande.
- Melhor de 3 por padrão. Se empatar no tempo, tem prorrogação.
- Modo Fúria: o time que está perdendo ganha pontos em dobro por 10s.
- Bônus automático pro time com menos gente.
- O placar da live acumula as vitórias de cada time.

## Editor

Aperta **E** (ou o botão ⚙️) pra abrir. Dá pra mudar nome, emoji, comando, cor e foto de cada time, e as regras (melhor de quantos, tempo do round, pontos por ação). Tudo aplica na hora.

Presets: salvar, carregar, apagar, exportar e importar um JSON de backup. Já vêm "Azul × Vermelho" e "Dexter × Mentalista", sem foto. Ficam no `localStorage` do navegador, então cada navegador tem os seus. Exporta pra levar pra outro lugar.

## Como usar

1. TikFinity aberto e conectado na live (WebSocket em `ws://localhost:21213`).
2. Abre o `index.html` e captura a janela no TikTok Live Studio ou no OBS. Fecha o editor antes de capturar, ou abre com `?clean=1` pra esconder o botão ⚙️.

Parâmetros na URL: `?clean=1`, `?speed=4` (acelera), `?ws=ws://localhost:PORTA/`. Espaço pula a fase e o editor tem botões de teste com espectadores falsos.

## Nota

Testei com espectadores falsos, não com o TikFinity de verdade.
