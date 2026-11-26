ï»¿# Motor de VêÂ­deos Narrativos

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


**[PortuguêÂªs](README.md) êÂ· [English](README.en.md) êÂ· [EspaêÂ±ol](README.es.md)**

[![Motor de VêÂ­deos Narrativos](guia/assets/banner.jpg)](https://inematds.github.io/motor-videos-narrativos/guia/)

## O que êÂ©

Uma ferramenta em Python para quem planeja vêÂ­deos educativos e narrativos. A partir de um assunto, organiza as cenas, os tempos previstos e as orientaêÂ§êÂµes de imagem, voz e mêÂºsica em dois arquivos. O histêÂ³rico local ajuda a variar as escolhas entre trabalhos. Basta ter Python 3.9 ou superior: a criaêÂ§êÂ£o do plano funciona offline, sem chave de API. O roteiro final, o êÂ¡udio e o vêÂ­deo sêÂ£o produzidos depois, com outras ferramentas.

## Guia de uso

[Abra o guia completo](https://inematds.github.io/motor-videos-narrativos/guia/).

```bash
git clone https://github.com/inematds/motor-videos-narrativos.git
cd motor-videos-narrativos
python3 motor_video.py --tema "Como o cafêÂ© chegou ao Brasil" --duracao 60 --formato 9:16
```

SaêÂ­das: `jobs/<id>/plano.json` e `jobs/<id>/prompt_pack.md`. O histêÂ³rico local `history.json` êÂ© criado automaticamente e nêÂ£o êÂ© versionado. Os exemplos recebidos estêÂ£o em `exemplos/`, incluindo o histêÂ³rico original.

- Python 3.9+, somente biblioteca padrêÂ£o; sem APIs ou pacotes externos.
- `--help`: lista todas as opêÂ§êÂµes; duraêÂ§êÂ£o entre 20 e 600 segundos.
- `--voz informative_warm`: seleciona um perfil do catêÂ¡logo; nêÂ£o sintetiza êÂ¡udio.
- `--seed`: repete escolhas apenas com os mesmos argumentos, configuraêÂ§êÂ£o e histêÂ³rico de entrada; metadados de data variam.
- `--out`: escolha uma pasta nova para evitar sobrescrever saêÂ­das anteriores.
- As escolhas sêÂ£o sorteios com restriêÂ§êÂµes de histêÂ³rico; nêÂ£o hêÂ¡ anêÂ¡lise semêÂ¢ntica do tema.
- O motor gera orientaêÂ§êÂµes e espaêÂ§os para roteiro. NêÂ£o pesquisa fatos, nêÂ£o escreve o roteiro final e nêÂ£o renderiza MP4.

## Materiais

- [DNA audiovisual](reference_analysis.md): anêÂ¡lise fornecida, com mediêÂ§êÂµes relatadas da referêÂªncia.
- [Proposta original](docs/proposta-original.md): visêÂ£o completa do fluxo; inclui etapas ainda externas ao cêÂ³digo.
- [CafêÂ©](exemplos/demo_cafe/prompt_pack.md) e [rios](exemplos/demo_rios/prompt_pack.md): exemplos recebidos em portuguêÂªs.
- `engine_config.json`: estruturas narrativas, linguagens visuais, vozes, mêÂºsica e regras de produêÂ§êÂ£o.

O ZIP recebido contêÂ©m o mesmo motor e configuraêÂ§êÂ£o dos arquivos avulsos; seus exemplos foram incorporados sem alterar o cêÂ³digo. O vêÂ­deo de referêÂªncia e a transcriêÂ§êÂ£o nêÂ£o vieram no pacote. As referêÂªncias a esses arquivos nos documentos originais sêÂ£o preservadas como contexto.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>