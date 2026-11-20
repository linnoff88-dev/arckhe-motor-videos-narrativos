# Motor de VÃ­deos Narrativos

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


**[PortuguÃªs](README.md) Â· [English](README.en.md) Â· [EspaÃ±ol](README.es.md)**

[![Motor de VÃ­deos Narrativos](guia/assets/banner.jpg)](https://inematds.github.io/motor-videos-narrativos/guia/)

## O que Ã©

Uma ferramenta em Python para quem planeja vÃ­deos educativos e narrativos. A partir de um assunto, organiza as cenas, os tempos previstos e as orientaÃ§Ãµes de imagem, voz e mÃºsica em dois arquivos. O histÃ³rico local ajuda a variar as escolhas entre trabalhos. Basta ter Python 3.9 ou superior: a criaÃ§Ã£o do plano funciona offline, sem chave de API. O roteiro final, o Ã¡udio e o vÃ­deo sÃ£o produzidos depois, com outras ferramentas.

## Guia de uso

[Abra o guia completo](https://inematds.github.io/motor-videos-narrativos/guia/).

```bash
git clone https://github.com/inematds/motor-videos-narrativos.git
cd motor-videos-narrativos
python3 motor_video.py --tema "Como o cafÃ© chegou ao Brasil" --duracao 60 --formato 9:16
```

SaÃ­das: `jobs/<id>/plano.json` e `jobs/<id>/prompt_pack.md`. O histÃ³rico local `history.json` Ã© criado automaticamente e nÃ£o Ã© versionado. Os exemplos recebidos estÃ£o em `exemplos/`, incluindo o histÃ³rico original.

- Python 3.9+, somente biblioteca padrÃ£o; sem APIs ou pacotes externos.
- `--help`: lista todas as opÃ§Ãµes; duraÃ§Ã£o entre 20 e 600 segundos.
- `--voz informative_warm`: seleciona um perfil do catÃ¡logo; nÃ£o sintetiza Ã¡udio.
- `--seed`: repete escolhas apenas com os mesmos argumentos, configuraÃ§Ã£o e histÃ³rico de entrada; metadados de data variam.
- `--out`: escolha uma pasta nova para evitar sobrescrever saÃ­das anteriores.
- As escolhas sÃ£o sorteios com restriÃ§Ãµes de histÃ³rico; nÃ£o hÃ¡ anÃ¡lise semÃ¢ntica do tema.
- O motor gera orientaÃ§Ãµes e espaÃ§os para roteiro. NÃ£o pesquisa fatos, nÃ£o escreve o roteiro final e nÃ£o renderiza MP4.

## Materiais

- [DNA audiovisual](reference_analysis.md): anÃ¡lise fornecida, com mediÃ§Ãµes relatadas da referÃªncia.
- [Proposta original](docs/proposta-original.md): visÃ£o completa do fluxo; inclui etapas ainda externas ao cÃ³digo.
- [CafÃ©](exemplos/demo_cafe/prompt_pack.md) e [rios](exemplos/demo_rios/prompt_pack.md): exemplos recebidos em portuguÃªs.
- `engine_config.json`: estruturas narrativas, linguagens visuais, vozes, mÃºsica e regras de produÃ§Ã£o.

O ZIP recebido contÃ©m o mesmo motor e configuraÃ§Ã£o dos arquivos avulsos; seus exemplos foram incorporados sem alterar o cÃ³digo. O vÃ­deo de referÃªncia e a transcriÃ§Ã£o nÃ£o vieram no pacote. As referÃªncias a esses arquivos nos documentos originais sÃ£o preservadas como contexto.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>