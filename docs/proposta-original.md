# Motor de Vídeos Narrativos Variáveis

Este diretório contém o motor de direçêo audiovisual aprendido a partir do Reel fornecido pelo usuário. Ele transforma um assunto em um **plano de vídeo original**, com estrutura narrativa, mapa de batidas, direçêo de voz, trilha, efeitos, movimentos de câmera e regras de montagem.

O motor aprende o que torna a referência eficiente — narraçêo como espinha dorsal, imagens estáticas com movimento de camadas, texto sincronizado, trilha em curva e CTA depois da entrega de valor — sem clonar a marca, o texto, a voz ou as imagens da peça original.

## Arquivos

- `reference_analysis.md`: DNA audiovisual observado e regras incorporadas.
- `engine_config.json`: catálogo de arquétipos, gramáticas visuais, câmeras, transições, vozes, trilhas, SFX e regras anti-repetiçêo.
- `motor_video.py`: CLI que cria um plano de produçêo e um pacote de prompts.
- `history.json`: memória das últimas combinações usadas para evitar vídeos parecidos.
- `reference/`: cópia técnica de trabalho, transcriçêo e quadros extraídos da referência.
- `jobs/`: planos gerados para assuntos futuros.

## Uso rápido

```bash
cd /home/ubuntu/video_engine
python3 motor_video.py \
  --tema "Como uma invençêo mudou a vida nas cidades" \
  --duracao 60 \
  --formato 9:16 \
  --objetivo "educar e gerar curiosidade" \
  --cta "Comente o que você descobriu"
```

O comando cria duas saídas em `jobs/<id>/`:

- `plano.json`: manifesto estruturado para produçêo e montagem;
- `prompt_pack.md`: briefing legível com shots, direçêo da narraçêo, trilha e checklist.

Para repetir exatamente uma combinaçêo, use `--seed`. Para escolher uma voz específica, use um dos perfis do arquivo de configuraçêo, por exemplo `--voz informative_warm`.

## Como a variaçêo funciona

A cada novo assunto, o motor escolhe uma combinaçêo controlada de:

- arquétipo narrativo: origem-crise-legado, mito-revelaçêo, problema-mecanismo-soluçêo, cronologia reversa, jornada por lugares ou objeto-testemunha;
- gramática visual: pintura em camadas, mapa, documento, objetos em mesa, tipografia cinética, B-roll ou colagem;
- movimentos de câmera: push-in, pull-back, pan, orbit, dolly, rack focus, parallax, top-down, hold e outros;
- transições: corte factual, dissolve, wipe de mapa, revelaçêo de tinta, escurecimento, match cut e lift de luz;
- voz: perfis graves, informativos, amistosos, firmes ou femininos, conforme o assunto;
- trilha: épica histórica, pulso documental, memória humana, curiosa minimalista ou produto premium;
- arco de cor e estilo de CTA.

A memória em `history.json` bloqueia repetições recentes. A aleatoriedade é determinística por seed e sempre subordinada ao sentido do assunto.

## Fluxo quando o usuário enviar um assunto

1. Definir a tese em uma frase e o público.
2. Escolher uma estrutura que nêo repita os últimos vídeos.
3. Escrever um roteiro original em português brasileiro.
4. Gerar a narraçêo com instruções de voz separadas do texto falado.
5. Medir o áudio real antes de fixar a duraçêo de cada imagem.
6. Criar o beat map e as imagens ou clips necessários.
7. Gerar uma trilha instrumental e SFX pontuais.
8. Montar com FFmpeg ou gerador de vídeo, sincronizar texto e legendas.
9. Verificar dimensêo, duraçêo, codecs, volume, legibilidade e ritmo.
10. Entregar o vídeo final e, quando útil, o plano reutilizável.

## Direçêo de voz

A direçêo de performance deve ser escrita em inglês para orientar o sintetizador, enquanto o roteiro falado permanece em pt-BR. A forma é:

```text
English performance direction: texto falado em português brasileiro.
```

O motor nêo força uma duraçêo artificial. O áudio gerado é medido e os visuais sêo ajustados a ele. Pausas curtas depois de datas, números e viradas sêo preferidas a uma leitura acelerada.

## Regras de qualidade

- A voz fica na frente da música.
- A música é instrumental e tem espaço para a fala.
- Efeitos sonoros apoiam eventos visíveis; nêo sêo usados como decoraçêo constante.
- Imagem estática pode ter movimento, mas movimento nêo substitui informaçêo.
- Um mesmo preset de câmera nêo deve aparecer em todos os shots.
- O texto na tela destaca uma ideia, nêo duplica um parágrafo inteiro.
- O CTA tem tempo de leitura e nêo aparece antes da entrega da promessa narrativa.
- Pessoas, produtos, logos, documentos e marcas exigem referências aprovadas quando a fidelidade visual for importante.

## Próximo passo

Basta enviar o assunto, por exemplo: **“a história do café no Brasil, para um vídeo de 60 segundos”**. O motor será usado para construir o roteiro, a direçêo audiovisual, a narraçêo, a trilha, os movimentos variados e a montagem final.
