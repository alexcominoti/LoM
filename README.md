# Legend of Mana (PSX) — Tradução PT-BR

Tradução para português do Brasil do Legend of Mana de PlayStation (versão americana).

**[⬇ Baixar a versão mais recente](https://github.com/alexcominoti/LoM/releases/latest)**

## O que está traduzido (v1.1.0)

- Todos os diálogos, enciclopédias e menus.
- Imagens: logo e tela de título, títulos dos eventos, telas de fim de evento, telas de ajuda, mapa-múndi
  (lugares, artefatos e espíritos), telas de terra, nomes de armas e menus, efeitos de batalha e a grade de
  lógica do golem.
- Vídeos legendados: a abertura cantada (karaokê) e as falas do início dos créditos finais.

### Novidades da v1.1.0

- A imagem da title screen foi traduzida para "A Lenda de Mana".
- Mapa-múndi: nomes dos lugares e dos artefatos traduzidos.
- Títulos dos eventos e telas de fim de evento redesenhados.
- Telas de ajuda (SELECT) redesenhadas.
- Traduzidos: grade de lógica do golem (GIRAR, INÍCIO : FIM, DIST., ATAQ.), "DIÁRIO" no menu circular, "SAIR" na
  enciclopédia e "A Lenda de Mana" na tela de escolha do mapa.
- Tela de escolha de personagem e de arma redesenhada.
- Vídeos legendados: a abertura cantada (karaokê, letra traduzida do sueco) e as falas do início dos créditos
  finais.
- Fonte: inclusão de Ç maiúsculo; ajustes feitos em Á, É, Í, Ó, Ú, ê e ç.
- Pequenas correções: correção no nome de alguns equipamentos que herdavam trechos de palavra do dicionário
  americano; separação entre material e tipo nos nomes das armas; atributos em caixa alta na tela de status;
  falas que passavam da caixa de diálogo e palavras que sobravam sozinhas numa linha; técnica “Super Rebatedor”
  renomeada para “Superrebatida”; ajustes pequenos em diálogos.

## O que você precisa

A imagem **original americana** do jogo, em um único arquivo `.bin`:

| | |
|---|---|
| Arquivo | `Legend of Mana (USA).bin` |
| Tamanho | 677.406.576 bytes |
| CRC32 | `5028946F` |

Um `.iso` de 2048 bytes por setor ou um `.bin` já modificado não servem.

## Como aplicar

### Arrastar e soltar (Windows)

1. Baixe o `.zip` da [release](https://github.com/alexcominoti/LoM/releases/latest) e extraia a pasta inteira.
2. Arraste o `.bin` original em cima de `aplicar_patch.bat`.
3. Quando aparecer "Pronto!", a pasta vai ter `Legend of Mana (PT-BR).bin` e `Legend of Mana (PT-BR).cue`.
4. Abra o `.cue` no emulador (DuckStation, ePSXe, Mednafen/Beetle PSX...). O `.bin` original não é alterado.

### Linha de comando / outros sistemas

```
xdelta3 -d -s "Legend of Mana (USA).bin" "Legend of Mana PT-BR v1.1.0.xdelta" "Legend of Mana (PT-BR).bin"
```

Depois crie `Legend of Mana (PT-BR).cue` com:

```
FILE "Legend of Mana (PT-BR).bin" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
```

Também dá para usar o [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher) ou o [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/).

### Como conferir

O `.bin` traduzido da v1.1.0 tem **672.041.664 bytes** e CRC32 **`15FF8559`**. Ele é menor que o original
porque a ferramenta de inserção remonta o CD de forma mais compacta. Se o xdelta acusar erro de checksum, a
imagem de origem não é a original americana.

### Atualizando de uma versão anterior

Aplique sempre o patch sobre o `.bin` **original americano**, nunca sobre um já traduzido, e substitua o `.bin`
traduzido antigo. Os saves do cartão de memória continuam valendo.

## Créditos

- **Tradução PT-BR:** sm0ke
- **Ferramentas de extração/inserção (PSX-LoM-Tools):** BahaBulle
- **Apoio:** Green Goblin (tradução espanhola)
- **Logo "A Lenda de Mana" na title screen:** linxkidd

Novidades da tradução: https://legendofmanaproject.blogspot.com/

## Aviso

Projeto de fã, gratuito e sem fins lucrativos, sem ligação com a Square Enix. Legend of Mana é propriedade da
Square Enix. Este repositório contém apenas o patch de tradução: não contém o jogo nem a imagem do CD, e o patch
não funciona sem a sua própria cópia original. Não distribua a imagem do jogo, nem a original nem a traduzida.

O `xdelta3.exe` incluído no pacote é o xdelta 3.0.6, de Joshua MacDonald, sob a licença GPL
([código-fonte](https://github.com/jmacd/xdelta)).
